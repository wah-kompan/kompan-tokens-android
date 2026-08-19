# kompan-tokens-android

Host repository for the KOMPAN design tokens Android library.

The sources are **not** kept here — they are generated per release by
`@kompan-design/token-build` in `heavyy/kompan-design` and published straight to
this repository's Maven registry. This repo exists because GitHub Packages scopes
Maven artifacts to a repository, and that scoping is what makes access follow the
organisation's permissions.

## Install

```kotlin
repositories {
    maven {
        url = uri("https://maven.pkg.github.com/wah-kompan/kompan-tokens-android")
        credentials {
            username = providers.gradleProperty("gpr.user").get()
            password = providers.gradleProperty("gpr.key").get()
        }
    }
}

dependencies {
    implementation("com.kompan.design:tokens:<version>")
}
```

The token needs `read:packages`. See the design system's Installation guide.
