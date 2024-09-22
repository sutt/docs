# Working on Opensource Frontend: lb-next

## Quickstart for developing on lb-next

_Repo located here:_ [_https://github.com/Lightning-Bounties/lb-next/_](https://github.com/Lightning-Bounties/lb-next/)

#### Instructions for connecting local frontend to remote backend

_We don't want to click "sign in with github" on localhost, but instead add the jwt token directly to simulate signing in._

1. In `.env.local` set:
   1.  make this edit, don't forget http**s**

       `NEXT_PUBLIC_API_URL=https://app.lightningbounties.com`
   2. after reloading the page you should see the same bounties on the feed
2. Get the `accessToken` from app.lightningbounties.com
   1. Go to https://app.lightningbounties.com
   2. Open chrome developer tools, go to Application tab, go to Local storage.
   3. Find `accessToken` and sign-in with github on the browser.
   4. Copy the value of accessToken, it should begin with `Bearer eyJhbGc...`
3. Set `accessToken` on localhost:3000
   1. On your browser where you are viewing the local repo running on the next dev server, open dev tools to the Local storage, find an accessToken key or add it.
   2. Paste the value of the token into local storage (including the `Bearer` prefix).
   3. Reload the page on localhost:3000, and you should be signed in under your app.lightningbounties.com user.

#### Video of Setup

{% file src="../.gitbook/assets/set-jwt-localhost-1.mp4" %}

Or visit: [https://4191743023-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgvH1HLwrajw9XplSBFfy%2Fuploads%2FiHh8RbltxAwaS7x9H0wy%2Fset-jwt-localhost-1.mp4?alt=media\&token=99e8108e-a337-4532-bdd3-010577c112be](https://4191743023-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FgvH1HLwrajw9XplSBFfy%2Fuploads%2FiHh8RbltxAwaS7x9H0wy%2Fset-jwt-localhost-1.mp4?alt=media\&token=99e8108e-a337-4532-bdd3-010577c112be)



<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>
