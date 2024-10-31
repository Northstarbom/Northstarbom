

- 🌱 Quantum coding
- 💞️ We are looking to collaborate on Metaverse development
-     Metaverse currency

<!---
Northstarbom/Northstarbom is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.1;

// This is a smart contract - a program that can be deployed to the Ethereum blockchain.
contract SimpleToken {
    // An `address` is comparable to an email address - it's used to identify an account on Ethereum.
    address public owner;
    uint256 public constant token_supply = 1000000000000;

    // A `mapping` is essentially a hash table data structure.
    // This `mapping` assigns an unsigned integer (the token balance) to an address (the token holder).
    mapping (address => uint) public balances;


	// When 'SimpleToken' contract is deployed:
	// 1. set the deploying address as the owner of the contract
	// 2. set the token balance of the owner to the total token supply
    constructor() {
        owner = msg.sender;
        balances[owner] = token_supply;
    }

    // Sends an amount of tokens from any caller to any address.
    function transfer(address receiver, uint amount) public {
        // The sender must have enough tokens to send
        require(amount <= balances[msg.sender], "Insufficient balance.");

        // Adjusts token balances of the two addresses
        balances[msg.sender] -= amount;
        balances[receiver] += amount;
    }
}

{
    "_meta": {
        "hash": {
            "sha256": "88b2cb37754e29375a2a70c645208a8b877757c64c70f57868f215c5d44726da"
        },
        "pipfile-spec": 6,
        "requires": {
            "python_version": "3.7"
        },
        "sources": [
            {
                "name": "pypi",
                "url": "https://pypi.org/simple",
                "verify_ssl": true
            }
        ]
    },
    "default": {
        "certifi": {
            "hashes": [
                "sha256:1a4995114262bffbc2413b159f2a1a480c969de6e6eb13ee966d470af86af59c",
                "sha256:719a74fb9e33b9bd44cc7f3a8d94bc35e4049deebe19ba7d8e108280cfd59830"
            ],
            "version": "==2020.12.5"
        },
        "cffi": {
            "hashes": [
                "sha256:005a36f41773e148deac64b08f233873a4d0c18b053d37da83f6af4d9087b813",
                "sha256:0857f0ae312d855239a55c81ef453ee8fd24136eaba8e87a2eceba644c0d4c06",
                "sha256:1071534bbbf8cbb31b498d5d9db0f274f2f7a865adca4ae429e147ba40f73dea",
                "sha256:158d0d15119b4b7ff6b926536763dc0714313aa59e320ddf787502c70c4d4bee",
                "sha256:1f436816fc868b098b0d63b8920de7d208c90a67212546d02f84fe78a9c26396",
                "sha256:2894f2df484ff56d717bead0a5c2abb6b9d2bf26d6960c4604d5c48bbc30ee73",
                "sha256:29314480e958fd8aab22e4a58b355b629c59bf5f2ac2492b61e3dc06d8c7a315",
                "sha256:34eff4b97f3d982fb93e2831e6750127d1355a923ebaeeb565407b3d2f8d41a1",
                "sha256:35f27e6eb43380fa080dccf676dece30bef72e4a67617ffda586641cd4508d49",
                "sha256:3d3dd4c9e559eb172ecf00a2a7517e97d1e96de2a5e610bd9b68cea3925b4892",
                "sha256:43e0b9d9e2c9e5d152946b9c5fe062c151614b262fda2e7b201204de0b99e482",
                "sha256:48e1c69bbacfc3d932221851b39d49e81567a4d4aac3b21258d9c24578280058",
                "sha256:51182f8927c5af975fece87b1b369f722c570fe169f9880764b1ee3bca8347b5",
                "sha256:58e3f59d583d413809d60779492342801d6e82fefb89c86a38e040c16883be53",
                "sha256:5de7970188bb46b7bf9858eb6890aad302577a5f6f75091fd7cdd3ef13ef3045",
                "sha256:65fa59693c62cf06e45ddbb822165394a288edce9e276647f0046e1ec26920f3",
                "sha256:69e395c24fc60aad6bb4fa7e583698ea6cc684648e1ffb7fe85e3c1ca131a7d5",
                "sha256:6c97d7350133666fbb5cf4abdc1178c812cb205dc6f41d174a7b0f18fb93337e",
                "sha256:6e4714cc64f474e4d6e37cfff31a814b509a35cb17de4fb1999907575684479c",
                "sha256:72d8d3ef52c208ee1c7b2e341f7d71c6fd3157138abf1a95166e6165dd5d4369",
                "sha256:8ae6299f6c68de06f136f1f9e69458eae58f1dacf10af5c17353eae03aa0d827",
                "sha256:8b198cec6c72df5289c05b05b8b0969819783f9418e0409865dac47288d2a053",
                "sha256:99cd03ae7988a93dd00bcd9d0b75e1f6c426063d6f03d2f90b89e29b25b82dfa",
                "sha256:9cf8022fb8d07a97c178b02327b284521c7708d7c71a9c9c355c178ac4bbd3d4",
                "sha256:9de2e279153a443c656f2defd67769e6d1e4163952b3c622dcea5b08a6405322",
                "sha256:9e93e79c2551ff263400e1e4be085a1210e12073a31c2011dbbda14bda0c6132",
                "sha256:9ff227395193126d82e60319a673a037d5de84633f11279e336f9c0f189ecc62",
                "sha256:a465da611f6fa124963b91bf432d960a555563efe4ed1cc403ba5077b15370aa",
                "sha256:ad17025d226ee5beec591b52800c11680fca3df50b8b29fe51d882576e039ee0",
                "sha256:afb29c1ba2e5a3736f1c301d9d0abe3ec8b86957d04ddfa9d7a6a42b9367e396",
                "sha256:b85eb46a81787c50650f2392b9b4ef23e1f126313b9e0e9013b35c15e4288e2e",
                "sha256:bb89f306e5da99f4d922728ddcd6f7fcebb3241fc40edebcb7284d7514741991",
                "sha256:cbde590d4faaa07c72bf979734738f328d239913ba3e043b1e98fe9a39f8b2b6",
                "sha256:cd2868886d547469123fadc46eac7ea5253ea7fcb139f12e1dfc2bbd406427d1",
                "sha256:d42b11d692e11b6634f7613ad8df5d6d5f8875f5d48939520d351007b3c13406",
                "sha256:f2d45f97ab6bb54753eab54fffe75aaf3de4ff2341c9daee1987ee1837636f1d",
                "sha256:fd78e5fee591709f32ef6edb9a015b4aa1a5022598e36227500c8f4e02328d9c"
            ],
            "version": "==1.14.5"
        },
        "chardet": {
            "hashes": [
                "sha256:0d6f53a15db4120f2b08c94f11e7d93d2c911ee118b6b30a04ec3ee8310179fa",
                "sha256:f864054d66fd9118f2e67044ac8981a54775ec5b67aed0441892edb553d21da5"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4'",
            "version": "==4.0.0"
        },
        "cryptography": {
            "hashes": [
                "sha256:2d32223e5b0ee02943f32b19245b61a62db83a882f0e76cc564e1cec60d48f87",
                "sha256:57ad77d32917bc55299b16d3b996ffa42a1c73c6cfa829b14043c561288d2799",
                "sha256:5ecf2bcb34d17415e89b546dbb44e73080f747e504273e4d4987630493cded1b",
                "sha256:66b57a9ca4b3221d51b237094b0303843b914b7d5afd4349970bb26518e350b0",
                "sha256:93cfe5b7ff006de13e1e89830810ecbd014791b042cbe5eec253be11ac2b28f3",
                "sha256:df186fcbf86dc1ce56305becb8434e4b6b7504bc724b71ad7a3239e0c9d14ef2",
                "sha256:fec7fb46b10da10d9e1d078d1ff8ed9e05ae14f431fdbd11145edd0550b9a964"
            ],
            "markers": "python_version >= '3.6'",
            "version": "==3.4.6"
        },
        "diem": {
            "hashes": [
                "sha256:0718ecc21b703ff285c148293dfcae21e780e2f1532b24a1a943561cb063c9e0",
                "sha256:6b9311ca5f671677eb4d1affafc39d720b8f44562dc8e7db961477d378777542"
            ],
            "index": "pypi",
            "version": "==1.2.5"
        },
        "idna": {
            "hashes": [
                "sha256:b307872f855b18632ce0c21c5e45be78c0ea7ae4c15c828c20788b26921eb3f6",
                "sha256:b97d804b1e9b523befed77c48dacec60e6dcb0b5391d57af6a65a312a90648c0"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
            "version": "==2.10"
        },
        "numpy": {
            "hashes": [
                "sha256:032be656d89bbf786d743fee11d01ef318b0781281241997558fa7950028dd29",
                "sha256:104f5e90b143dbf298361a99ac1af4cf59131218a045ebf4ee5990b83cff5fab",
                "sha256:125a0e10ddd99a874fd357bfa1b636cd58deb78ba4a30b5ddb09f645c3512e04",
                "sha256:12e4ba5c6420917571f1a5becc9338abbde71dd811ce40b37ba62dec7b39af6d",
                "sha256:13adf545732bb23a796914fe5f891a12bd74cf3d2986eed7b7eba2941eea1590",
                "sha256:2d7e27442599104ee08f4faed56bb87c55f8b10a5494ac2ead5c98a4b289e61f",
                "sha256:3bc63486a870294683980d76ec1e3efc786295ae00128f9ea38e2c6e74d5a60a",
                "sha256:3d3087e24e354c18fb35c454026af3ed8997cfd4997765266897c68d724e4845",
                "sha256:4ed8e96dc146e12c1c5cdd6fb9fd0757f2ba66048bf94c5126b7efebd12d0090",
                "sha256:60759ab15c94dd0e1ed88241fd4fa3312db4e91d2c8f5a2d4cf3863fad83d65b",
                "sha256:65410c7f4398a0047eea5cca9b74009ea61178efd78d1be9847fac1d6716ec1e",
                "sha256:66b467adfcf628f66ea4ac6430ded0614f5cc06ba530d09571ea404789064adc",
                "sha256:7199109fa46277be503393be9250b983f325880766f847885607d9b13848f257",
                "sha256:72251e43ac426ff98ea802a931922c79b8d7596480300eb9f1b1e45e0543571e",
                "sha256:89e5336f2bec0c726ac7e7cdae181b325a9c0ee24e604704ed830d241c5e47ff",
                "sha256:89f937b13b8dd17b0099c7c2e22066883c86ca1575a975f754babc8fbf8d69a9",
                "sha256:9c94cab5054bad82a70b2e77741271790304651d584e2cdfe2041488e753863b",
                "sha256:9eb551d122fadca7774b97db8a112b77231dcccda8e91a5bc99e79890797175e",
                "sha256:a1d7995d1023335e67fb070b2fae6f5968f5be3802b15ad6d79d81ecaa014fe0",
                "sha256:ae61f02b84a0211abb56462a3b6cd1e7ec39d466d3160eb4e1da8bf6717cdbeb",
                "sha256:b9410c0b6fed4a22554f072a86c361e417f0258838957b78bd063bde2c7f841f",
                "sha256:c26287dfc888cf1e65181f39ea75e11f42ffc4f4529e5bd19add57ad458996e2",
                "sha256:c91ec9569facd4757ade0888371eced2ecf49e7982ce5634cc2cf4e7331a4b14",
                "sha256:ecb5b74c702358cdc21268ff4c37f7466357871f53a30e6f84c686952bef16a9"
            ],
            "markers": "python_version >= '3.7'",
            "version": "==1.20.1"
        },
        "protobuf": {
            "hashes": [
                "sha256:0e247612fadda953047f53301a7b0407cb0c3cb4ae25a6fde661597a04039b3c",
                "sha256:0fc96785262042e4863b3f3b5c429d4636f10d90061e1840fce1baaf59b1a836",
                "sha256:1c51fda1bbc9634246e7be6016d860be01747354ed7015ebe38acf4452f470d2",
                "sha256:1d63eb389347293d8915fb47bee0951c7b5dab522a4a60118b9a18f33e21f8ce",
                "sha256:22bcd2e284b3b1d969c12e84dc9b9a71701ec82d8ce975fdda19712e1cfd4e00",
                "sha256:2a7e2fe101a7ace75e9327b9c946d247749e564a267b0515cf41dfe450b69bac",
                "sha256:43b554b9e73a07ba84ed6cf25db0ff88b1e06be610b37656e292e3cbb5437472",
                "sha256:4b74301b30513b1a7494d3055d95c714b560fbb630d8fb9956b6f27992c9f980",
                "sha256:4e75105c9dfe13719b7293f75bd53033108f4ba03d44e71db0ec2a0e8401eafd",
                "sha256:5b7a637212cc9b2bcf85dd828b1178d19efdf74dbfe1ddf8cd1b8e01fdaaa7f5",
                "sha256:5e9806a43232a1fa0c9cf5da8dc06f6910d53e4390be1fa06f06454d888a9142",
                "sha256:629b03fd3caae7f815b0c66b41273f6b1900a579e2ccb41ef4493a4f5fb84f3a",
                "sha256:72230ed56f026dd664c21d73c5db73ebba50d924d7ba6b7c0d81a121e390406e",
                "sha256:86a75477addde4918e9a1904e5c6af8d7b691f2a3f65587d73b16100fbe4c3b2",
                "sha256:8971c421dbd7aad930c9bd2694122f332350b6ccb5202a8b7b06f3f1a5c41ed5",
                "sha256:9616f0b65a30851e62f1713336c931fcd32c057202b7ff2cfbfca0fc7d5e3043",
                "sha256:b0d5d35faeb07e22a1ddf8dce620860c8fe145426c02d1a0ae2688c6e8ede36d",
                "sha256:ecc33531a213eee22ad60e0e2aaea6c8ba0021f0cce35dbf0ab03dee6e2a23a1"
            ],
            "version": "==3.14.0"
        },
        "pycparser": {
            "hashes": [
                "sha256:2d475327684562c3a96cc71adf7dc8c4f0565175cf86b6d7a404ff4c771f15f0",
                "sha256:7582ad22678f0fcd81102833f60ef8d0e57288b6b5fb00323d101be910e35705"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3'",
            "version": "==2.20"
        },
        "requests": {
            "hashes": [
                "sha256:27973dd4a904a4f13b263a19c866c13b92a39ed1c964655f025f3f8d3d75b804",
                "sha256:c210084e36a42ae6b9219e00e48287def368a26d03a048ddad7bfee44f75871e"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4'",
            "version": "==2.25.1"
        },
        "six": {
            "hashes": [
                "sha256:30639c035cdb23534cd4aa2dd52c3bf48f06e5f4a941509c8bafd8ce11080259",
                "sha256:8b74bedcbbbaca38ff6d7491d76f2b06b3592611af620f8426e82dddb04a5ced"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2'",
            "version": "==1.15.0"
        },
        "urllib3": {
            "hashes": [
                "sha256:1b465e494e3e0d8939b50680403e3aedaa2bc434b7d5af64dfd3c958d7f5ae80",
                "sha256:de3eedaad74a2683334e282005cd8d7f22f4d55fa690a2a1020a416cb0a47e73"
            ],
            "markers": "python_version >= '2.7' and python_version not in '3.0, 3.1, 3.2, 3.3, 3.4' and python_version < '4'",
            "version": "==1.26.3"
        }
    },
    "develop": {}
}
