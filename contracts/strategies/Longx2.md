# long x2

## Pseudo code

### Strategy entry

Instructions
- transfert_usdt_from_user_to_strat(amount)
- transfert_usdt_from_reserve_to_strat(2*amount)
- swap_usdt_to_wrap_xtz(2*amount, start_address)
- deposit_result_xtz_to_youves(start_address)
- borrow(amount)
- transfert_usdt_to_reserve(amount)
