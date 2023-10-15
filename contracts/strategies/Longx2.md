# long x2

## Pseudo code

### Strategy entry

Instructions
- transfert_usdt_from_user_to_strat(amount)
- transfert_usdt_from_reserve_to_strat(2*amount)
- swap_usdt_to_wrap_xtz(2*amount, start_address)
- deposit_result_xtz_to_youves(start_address)
- borrow(amount)
- swap_and_transfert_uusd_to_usdt(amount, pool_address)

### Close strategy (by user)

#### Instructions:

- check_postion_status(position_id)
- get_uusd_amount_borrowed(position_id) [included: borrow + interest]
- repay_uusd_borrowed(position_id, borrow_amount)
- redeem_xtz(position_id)
- swap_xtz_for_usdt()
- get_refund_reserve_amount(position_id)
- refund_reserve(position_id)
- transfert_profit_to_user()


### Liquidate position

- check_liquidation_requirements(position_id)
- check_postion_status(position_id) [included: borrow + interest]
- get_uusd_amount_borrowed(position_id)
- repay_uusd_borrowed(position_id, borrow_amount)
- redeem_xtz(position_id)
- swap_xtz_for_usdt()
- transfert_remaning_usdt_to_reserve(position_id) [refun amount + fees]

## Roadmap improvements:
- Add more levrage possibilities
- Add new levrage assets
- partial liquidation
- allow side party liquidators
