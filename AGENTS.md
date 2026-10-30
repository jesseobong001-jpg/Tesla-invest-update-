<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Country and city directories are loaded through server functions, keeping the large worldwide dataset out of browser bundles.
- Orders and investment deposits use one shared payment-method definition and picker so their available methods and receiving details stay consistent.
- Investment quotes use a shared six-asset catalog and server-side public feed with timestamp, delay caveat and 60-second polling; unavailable rates never get fabricated prices.
- Deposit proofs are private owner-scoped storage objects; authenticated server review saves submissions, and screenshot analysis never credits a wallet without independent settlement verification.
- Wallet writes and multi-asset allocations use atomic owner-scoped database functions; clients have read-only access, legacy TSLA totals are backfilled, and allocations never claim external trade execution.
- Shared page sections take the signed-in user as a prop instead of calling another route's `Route.useRouteContext()`, because a borrowed route match throws an invariant error on any page that is not that route.
- The shared nav bar carries only the brand and page links; account actions such as signing out live in the shared footer band, so the nav stays readable on phone widths.
