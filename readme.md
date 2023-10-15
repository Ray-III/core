# Bull Finance

## Strategies implemented

### Long x2 Strategy
<img src="illustrations/Long_implemented_strategy.png" alt="Long x2 Strategy"/>

### Short x2 Strategy
<img src="illustrations/Short_implemented_startegy.png" alt="Short x2 Strategy"/>


### Deployments

Permit: KT1XMTxQJNaSHLPChYeDU2h4HqUBCPkW8jQP
USDT: KT1FVu8JQjCMLeeNFhrzXkFViFHxnV9TYM6Z
uUSD: KT19QkeKzaHaAJGSRqH8ijF1pkgbvTNQkjfU
oracle: KT1LKSNYYx2bhQ15MnETSakzqFfNoq2oSgaY
`completium-cli deploy ./contracts/mocks/oracle.arl`
swap: KT1C3oJyAuCjEiCmnvdhBuaSw9iRR3sxWBKN
`completium-cli deploy ./contracts/mocks/swap.arl --parameters '{"usdt": "KT1FVu8JQjCMLeeNFhrzXkFViFHxnV9TYM6Z", "uusd": "KT19QkeKzaHaAJGSRqH8ijF1pkgbvTNQkjfU", "oracle_address": "KT1LKSNYYx2bhQ15MnETSakzqFfNoq2oSgaY"}'`

- send 1M USDT to swap
- send 1M UUSD to swap
- send tez to swap

tez_engine: KT1UAhaGhz5Hj1YU5XzGu491UToZAght4Bha
`completium-cli deploy ./contracts/mocks/tez_v3engine.arl --parameters '{"oracle_address": "KT1LKSNYYx2bhQ15MnETSakzqFfNoq2oSgaY", "uusd_address": "KT19QkeKzaHaAJGSRqH8ijF1pkgbvTNQkjfU"}'`
lp: KT1HghtHsRciB7uYWye1qMxUcEtVG3xaU8Zy
`completium-cli deploy ./contracts/interfaces/fa2.arl --parameters '{"owner": "tz1LunH1MzRTpMx6HoWxnmpburbSNaxHCumV", "permits": "KT1XMTxQJNaSHLPChYeDU2h4HqUBCPkW8jQP"}' --named lp`

- set token metadata

pool: KT1MxhBqikJ1GpHSLHyKi44Mc4RwbrCW95dV
`completium-cli deploy ./contracts/pool.arl --parameters '{"owner": "tz1LunH1MzRTpMx6HoWxnmpburbSNaxHCumV", "token": "KT1FVu8JQjCMLeeNFhrzXkFViFHxnV9TYM6Z", "token_id": 0}' --named pool`
long:
`completium-cli deploy ./contracts/strategies/long.arl --parameters '{"usdt": "KT1FVu8JQjCMLeeNFhrzXkFViFHxnV9TYM6Z", "reserve": "KT1MxhBqikJ1GpHSLHyKi44Mc4RwbrCW95dV", "engine": "KT1UAhaGhz5Hj1YU5XzGu491UToZAght4Bha", "uusd": "KT19QkeKzaHaAJGSRqH8ijF1pkgbvTNQkjfU", "uusd_id": 0, "swap_address": "KT1C3oJyAuCjEiCmnvdhBuaSw9iRR3sxWBKN"}' --named long-xtz`
