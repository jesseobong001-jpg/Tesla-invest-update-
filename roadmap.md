# Roadmap

- [done] Country-first city selection in car orders; verified Nigeria → Lagos and successful order submission
- [done] Shared six payment methods and receiving details for orders and deposits
- [done] Actual Tesla market data displayed on site; verified signed-in quote, timestamp, and market statistics
- [done] Deposit confirmation with private screenshot upload and real AI review; verified a non-payment image was flagged and balance stayed $0
- [ ] Automatic balance credit awaits independently verified payment receipt from connected payment services or real crypto receiving addresses; screenshots alone cannot prove settlement
- [done] Test new-account signup: immediately signed in and reached /reserve without email confirmation in the live browser

- [done] Deposit button opens a deposit dialog: crypto (BTC, USDT, Ethereum) or cash transfer (Cash App, PayPal, Zelle); original simulated instant-credit flow replaced by proof submission
- [done] Deposit dialog shows payment details: crypto options show address "adress1235388", cash options show "test@1234.com", each with a Copy button — verified for Ethereum and Cash App
- [done] Remix setup: copied Drizzle migrations cleared, fresh empty migration set scaffolded (validates clean); tables + access rules already live in the database
- [done] Side fixes: "New here? Create an account" toggle no longer submits the sign-in form; backend's weak-password rejection (6+ char rule) disabled
- [done] Remix backend reconfigured again (settings do not carry over): weak-password check off, new accounts sign in with no email confirmation — verified a fresh signup landed straight on /reserve
- [done] Payment plans page crash fixed: the shared installment section now takes the signed-in user as a prop instead of borrowing the investment page's route context — verified all 8 cars, weekly/monthly toggle, and an order form offering Bitcoin/USDT/Ethereum plus Card

## Open
- [done] Add Apple, NVIDIA, Bitcoin, Ethereum and Solana investment allocations with automatically refreshed rates for every asset
- [done] Verify multi-asset allocation security, current-rate display and investment selection — all six assets show rates, picking Ethereum switches the invest target to "Invest · ETH" (no live investment placed)
- [x] Add more Tesla models to the models list (same card + Order flow as existing ones)
- [x] Verify country→state picker (search removed) end-to-end in the preview

- [x] Card option replaces Cash App/PayPal/Zelle (no card numbers collected)
- [x] Pay-by-installment plans on investment page
- [ ] Real card checkout — blocked: needs a payment provider
