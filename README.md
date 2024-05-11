# ckb-spv-monit

## start CKB PRV 
```angular2html
cargo run 
```

#### get_spv_client

```angular2html
curl -X POST -H "Content-Type: application/json" \
    -d '{"id": 42, "jsonrpc": "2.0", "method": "get_ckb_client_message", "params": ["https://testnet.ckb.dev/", "c8a30fe3e8101cb4163e70b4eb1e42d477ae7094524a30bfdf1c90be41876d28", "3940bc9a03f7d4a92edd2065623a2f6bff96c9924aaf141cce2b2137776998d80a00"]}' \
    http://127.0.0.1:3000


{"jsonrpc":"2.0","result":[{"headers_mmr_root":{"children_hash":"8ff677c88b19693e7cb51eead68487dff3d8fa2a3e6c47e906eec6c95d66a7a9","max_height":837197,"min_height":834624,"partial_chain_work":"926111547494911420326204480"},"id":5,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"0000000000000000000266d8427f15f68c7519211c87d1da596fb2e419311665"},{"headers_mmr_root":{"children_hash":"4f5a248263ecf19df8483487bc2811912c23360724005d8fcb282d6793a638a3","max_height":837196,"min_height":834624,"partial_chain_work":"925754514312027309696104736"},"id":4,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"00000000000000000000c839bae945d1c6d3247a15d23f5241f889ce9da0ab92"},{"headers_mmr_root":{"children_hash":"ae1c4f9c6192a4e155a30457d78128263a589039f0daf9d73b95128ac25654bc","max_height":837194,"min_height":834624,"partial_chain_work":"925040447946259088435905248"},"id":3,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"000000000000000000030565da5f84e33ebcca2202da879774ac05ab892e67ba"},{"headers_mmr_root":{"children_hash":"f2e52a1e391301f0b6d678c6327563bccc285de2ba385c302fb508929e3e5590","max_height":837193,"min_height":834624,"partial_chain_work":"924683414763374977805805504"},"id":2,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"00000000000000000000e0e76462234b84396b825d7dd780e4e3141f53a8ca14"},{"headers_mmr_root":{"children_hash":"6b47b967ca20907432de8ec2f9ffa8d4124ab68e4df1fbf1c996e35188170a5a","max_height":837192,"min_height":834624,"partial_chain_work":"924326381580490867175705760"},"id":1,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"000000000000000000006e9dfcda4887a9f2b2206c683970853a538a98500dc5"},{"headers_mmr_root":{"children_hash":"8af5604dd7230d1a186bf4c37ee790fdf6a8be6ef009efc7b73e55a7463876b8","max_height":837191,"min_height":834624,"partial_chain_work":"923969348397606756545606016"},"id":0,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"00000000000000000002d8efac7e2327870b3cba00e805a165103136a67eb08e"},{"headers_mmr_root":{"children_hash":"3d33bace85629900de7f027ff750564ffd801c511674fc81bd0cbfb1b1fcc55d","max_height":837190,"min_height":834624,"partial_chain_work":"923612315214722645915506272"},"id":9,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"00000000000000000000070a6f73ab2aee52dd75a1a203f745c873293d9bb5c8"},{"headers_mmr_root":{"children_hash":"219923550676def2203cbe9f66ad5ebb0dd15b807c7b1e3a0753881a24861d9a","max_height":837189,"min_height":834624,"partial_chain_work":"923255282031838535285406528"},"id":8,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"000000000000000000002f7e9d25a54413da83a31f442d7049a491b3c0afcd9b"},{"headers_mmr_root":{"children_hash":"d13eef8014c34d57109ac2e68088597c09b3b7a9407dc1c270ceeb572e2ab15e","max_height":837188,"min_height":834624,"partial_chain_work":"922898248848954424655306784"},"id":7,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"000000000000000000010934419aac8cc72344b09f41af891e80d35ee8dcc718"},{"headers_mmr_root":{"children_hash":"4e2247e78d2f93dea5f2501810d9ee1abf430ccdd6e841821df5540eabe4c204","max_height":837187,"min_height":834624,"partial_chain_work":"922541215666070314025207040"},"id":6,"target_adjust_info":{"next_compact_target":"386097875","start_time":"1711619463"},"tip_block_hash":"0000000000000000000026da73f67fe8c0b7a3cb4421c2365755e0b44303256e"}],"id":42}%                                      
```
#### verify
```angular2html
curl -X POST -H "Content-Type: application/json" \
    -d '{"id": 42, "jsonrpc": "2.0", "method": "verify_tx", "params": ["ad03000014000000180000001c000000f90100000000000043c60c00d90100000020812f1ea566fdc775226e60cdd66591bd47c0da8604f4cbea00000000000000000000c2b56d118d869abfe89a12affef3bef141600b76e4b45f3fac0e269ee2f5c07f1c2f0a66d36203176f74ee582b0600000c8374f265338fe97826cc05e675bb1fc1a7edda56a914dca6297d345fd5bed6be23175ae97e32228af6112284502e9b77558c4a00e04e88b722147af2ee38c7309dd70aebe793fcbfda49eac97d7acb3bd6faffa11182b1c7a805d19cc15c5ce9f4ea7123d25f83b9bde9fa34d1758256c2f1e4c8b5527a9a7f2bc89c37fa09310c5bd66d4681aa72735398cad3d56fd631328c9d4dc329764368cb066062d343756123b11d1204226ffd2ef656d2cf714df5be688b92e668730ab66424bebaa9e0324ef5f70db2a5361bbac670348e52cc90c8d6254407bbd6db0eb7fbd04932ae88c2d93f2ef44ad045d62e9921acbb8873d62d38c981ada2f6b05ac35030fbdf8fc781b8e948e8b774eb92984cf5c7dc41b77bd5e6901e839c4a1c78ec5f3f8bb7fe02e39e5b21f665390a060b9d5c2cb42fd973fe8913491279454ceee6c1d38b3e2639f3254f4199bb1788c89cc296aef55e82ca3e6348becb6ff033c49c7e56e1a3a15d2163ee012a154ee68e01082d89c0033ef778deb3b7651de4fb6f03ff0f000600000040bc0c003fc40c0080180f8ef12bbbc6aab7620200000000000000000000000000000000000000006c8ccf5ef0b5d178bdd248d0d7707a3fb27f028f13876acfebcc92f99e7ba49940c40c003fc60c000040365f74723c819d35970000000000000000000000000000000000000000009e5b8daf5bd7b2cfa93fd466e389edc279da5b6d0be5a1dd9791f9d6419abc3442c60c0042c60c00209b2f3a399ec0ce9a4b000000000000000000000000000000000000000000001ea566fdc775226e60cdd66591bd47c0da8604f4cbea0000000000000000000040c60c0041c60c0040365f74723c819d3597000000000000000000000000000000000000000000009a95ea96bd7e4a0d699a9d2241bd3363986e1f1c1fe87c46a32c2211d2703c8244c60c0047c60c00806cbee8e478023b6b2e0100000000000000000000000000000000000000000053ea95a1ab3268374b4e1244ccc83f299b70083321d16f90cbff62438a36b71648c60c004dc60c00c0a21d5d57b583d8a0c501000000000000000000000000000000000000000000447de0c30b05d87526ddbef58bfd8a1e826d27e523722998848dce563eac5b3b", "bed6bed55f347d29a6dc14a956daeda7c11fbb75e605cc2678e98f3365f27483", "0565163119e4b26f59dad1871c2119758cf6157f42d8660200000000000000000040bc0c004dc60c0040d4df1b87458096bf0ffe020000000000000000000000000000000000000000a9a7665dc9c6ee06e9476c3e2afad8f3df8784d6ea1eb57c3e69198bc877f68f873d0566d3620317"]}' \
    http://127.0.0.1:3000

{"jsonrpc":"2.0","result":{"bits":386097875,"merkle_root":"7fc0f5e29e260eac3f5fb4e4760b6041f1bef3feaf129ae8bf9a868d116db5c2","nonce":1492022383,"prev_blockhash":"00000000000000000000eacbf40486dac047bd9165d6cd606e2275c7fd66a51e","time":1711943452,"version":796991488},"id":42}
```

### start monit
add discord `TOKEN` to `scripts/.env`
```angular2html
cd scripts
pip install -r  requirements.txt
python monit.py
```

### start prometheus
```angular2html
cd scripts
python prometheus.py
```