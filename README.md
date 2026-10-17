# boynepe.github.io

Public website, published with GitHub Pages at <https://boynepe.github.io/>.
Each app gets its own subdirectory; the root page is an index of them.

## `/mneme/`

Support, privacy and terms pages for Mneme, a lyric memorization app for
iPhone. Source in the private `Mneme` repo; `Docs/site.md` there lists what
points at each URL. The same rule as Nofret's: `/mneme/privacy` and
`/mneme/terms` are compiled into `PaywallView.swift`, and the listing names
`/mneme/`, `/mneme/privacy` and `/mneme/support`, so **they must not change**.
The privacy page claims Mneme collects nothing; it, the App Store privacy
answers and `Mneme/PrivacyInfo.xcprivacy` change together or not at all.

## `/nofret/`

Support, privacy and terms pages for [Nofret](https://boynepe.github.io/nofret/),
a guitar fretboard trainer for iPhone. The app source lives in the private
`Nofret` repo — this holds only the public pages.

Four of these URLs are referenced by the shipped app or its App Store listing,
so **they must not change**:

| URL | Referenced by |
|---|---|
| `/nofret/` | App Store "Marketing URL" (`Metadata/en-US/marketing_url.txt`) |
| `/nofret/privacy` | App Store "Privacy Policy URL"; `PaywallView.swift` |
| `/nofret/support` | App Store "Support URL" |
| `/nofret/terms` | `PaywallView.swift` — required by App Store guideline 3.1.2 |

Each page is a directory containing `index.html`, because the URLs compiled
into the app are extensionless and cannot change without a new build.
`.nojekyll` skips Jekyll processing; this is plain static HTML.

The privacy policy states that Nofret collects nothing. That is a claim about
the code, and it has to stay true: if the app ever gains analytics, crash
reporting, or sync, this page, the App Store Connect privacy answers, and
`PrivacyInfo.xcprivacy` all have to change in the same release.
