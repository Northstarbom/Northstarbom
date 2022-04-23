- 👋 Hi, I’m @Northstarbom
- 👀 I’m interested in ... Meta platforms
- 🌱 I’m currently learning ... Quantum coding
- 💞️ I’m looking to collaborate on ... Metaverse development
- 📫 How to reach me ... Bomlaqi@gmail.com

<!---
Northstarbom/Northstarbom is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

name: first North

on: [push]

env:
  NPM_TOKEN: ${{secrets.NPM_TOKEN}}

jobs:
  buildx:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Set up QEMU
        uses: docker/setup-qemu-action@v1
      - name: Set up Docker Buildx
        uses: docker/setup-buildx-action@v1
        id: buildx
        with:
          install: true
          buildkitd-flags: --debug
      - name: Cache Docker layers
        uses: actions/cache@v2
        with:
          path: /tmp/.buildx-cache
          key: ${{ runner.os }}-buildx-${{ github.sha }}
          restore-keys: |
            ${{ runner.os }}-buildx-
      - name: Bake Docker Image
        uses: docker/build-push-action@v2
        with:
          context: .
          builder: ${{ steps.buildx.outputs.name }}
          push: false
          tags: user/myimage:latest
          secrets: |
            "NPM_TOKEN=${{secrets.NPM_TOKEN}}"
          cache-from: type=local,src=/tmp/.buildx-cache
          cache-to: type=local,dest=/tmp/.buildx-cache-new
      - name: Available platforms
        run: echo ${{ steps.buildx.outputs.platforms }}
      - name: Lint and Test
        run: docker image ls -a
      # This ugly bit is necessary if you don't want your cache to grow forever
      # till it hits GitHub's limit of 5GB.
      # Temp fix
      # https://github.com/docker/build-push-action/issues/252
      # https://github.com/moby/buildkit/issues/1896
      - name: Move cache
        run: |
          rm -rf /tmp/.buildx-cache
          mv /tmp/.buildx-cache-new /tmp/.buildx-cache

- name: Set up Docker Buildx
        uses: docker/setup-buildx-action@v1
        id: buildx
        with:
          install: true
          buildkitd-flags: --debug
- name: Bake Docker Image
        run: |
          echo ${{secrets.NPM_TOKEN}}
          echo ${{secrets.NPM_TOKEN}} > NPM_TOKEN.txt
          cat NPM_TOKEN.txt
          docker build -t myimage:latest --progress=plain --secret id=NPM_TOKEN,src=NPM_TOKEN.txt .
          docker image ls -a
- name: Test
        run: docker image ls -a

REPOSITORY          TAG               IMAGE ID       CREATED        SIZE
100
moby/buildkit       buildx-stable-1   440639846006   38 hours ago   142MB
101
node                12-alpine         8dc0ee810c0a   3 days ago     91MB
102
node                14-alpine         6f5dba13ae83   3 days ago     119MB
103
node                16-alpine         59b389513e8a   3 days ago     111MB
104
alpine              3.12              24c8ece58a1a   4 days ago     5.58MB
89
alpine              3.13              20e452a0a81a   4 days ago     5.61MB
90
alpine              3.14              e04c818066af   4 days ago     5.59MB
91
node                12                543479162c86   9 days ago     918MB
92
node                14                7d03025aad90   9 days ago     945MB
93
node                16                424bc28f998d   9 days ago     906MB
94
buildpack-deps      stretch           de7321966554   10 days ago    835MB
95
buildpack-deps      buster            cbdff219ec50   10 days ago    804MB
96
buildpack-deps      bullseye          c93648763550   10 days ago    834MB
97
debian              9                 cb32206528ee   11 days ago    101MB
98
debian              10                76e02db62235   11 days ago    114MB
99
debian              11                d69c6cd3a20d   11 days ago    124MB
100
ubuntu              20.04             ff0fea8310f3   3 weeks ago    72.8MB
101
ubuntu              18.04             b67d6ac264e4   3 weeks ago    63.2MB
102
moby/buildkit       latest            ab57028900a2   4 weeks ago    142MB
103
tonistiigi/binfmt   latest            71d103174212   4 weeks ago    35.8MB
104
ubuntu              16.04             b6f507652425   7 months ago   135MB

the --mount option requires BuildKit. Refer to https://docs.docker.com/go/buildkit/ to learn how to build images with BuildKit enabled
31
Error: Process completed with exit code 1.

# syntax=docker/dockerfile:1.2

FROM alpine


# shows secret from default secret location:
RUN --mount=type=secret,id=NPM_TOKEN cat /run/secrets/NPM_TOKEN

CMD ["/bin/sh"]
