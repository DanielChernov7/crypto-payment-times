# How long a crypto payment takes, by network

Minutes from opening a payment window to a credited balance, from four months of real
top-ups on [NoctHost](https://nocthost.com), July to October 2026. The clock includes
the human part (copying the address, confirming in a wallet or exchange app) and the
network part (the transfer being mined and the confirmations the processor waits for),
so it is closer to what a payer actually waits than raw block times.

Write-up: https://nocthost.com/blog/crypto-payment-speed-by-network

## Results

| Method | Median | Slow case (p90) |
|---|---|---|
| Solana (SOL) | 1.6 min | 6.5 min |
| Card, for comparison | 2.3 min | 21 min |
| Ethereum (ETH) | 2.4 min | 2.9 min |
| USDT on BSC (BEP20) | 2.4 min | 7.1 min |
| USDT on Tron (TRC20) | 2.6 min | 12.2 min |
| USDT on Ethereum (ERC20) | 4.8 min | 10.1 min |
| Litecoin (LTC) | about 10 min | small sample |
| Bitcoin (BTC) | 16.5 min | 42 min |

## Files

- `data/crypto-payment-times-2026-07-to-10.csv`: one row per method. The first line is a `#` comment.

## Columns

- `method`: coin or card; `network`: chain the payment used
- `median_minutes`, `p90_minutes`: minutes from opening the payment window to the balance being credited (median, 90th percentile)
- `note`: caveats

## Limits

Real customer payments, not a controlled test: wallets, exchanges and fees vary. Networks
with too few payments and our own test payments are left out. Exchanges that batch or
review withdrawals add to the tail, especially on Tron.

## Cite

NoctHost (2026). *How long a crypto payment takes, by network*, July to October 2026.
https://nocthost.com/blog/crypto-payment-speed-by-network. Data under CC BY 4.0.

## License

Data in `data/`: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution: NoctHost, https://nocthost.com/blog/crypto-payment-speed-by-network
