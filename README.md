- 👋 Hi, I’m @Northstarbom
- 👀 I’m interested in ... Meta platforms
- 🌱 I’m currently learning ... Quantum coding
- 💞️ I’m looking to collaborate on ... Metaverse development
- 📫 How to reach me ... Bomlaqi@gmail.com

<!---
Northstarbom/Northstarbom is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


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
