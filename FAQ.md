Frequently Asked Questions
-

**Can I use JitPack with private repositories?**

Yes. See https://jitpack.io/private

**What happens if a tag is deleted on GitHub?**

If the project was already built JitPack will continue serving the existing artifacts. It will not rebuilt the project at the new tag. 
In case you need to redo a release the best option is to create a new version on GitHub.

**Will my builds be reproducible?**

Absolutely. Once JitPack builds a project it keeps the build artifacts (jar, aar, ... files) and continues to serve those for all subsequent builds.

**Is this like depending on source code repositories in other languages?**

Not really. With JitPack you specify which exact version you want and JitPack builds it. You can't have a dependency on the latest HEAD version. The author of the repository controls when to release a new version using GitHub's releases so from a consumer's perspective it's a typical package repository.

**How are the builds secured?**

Each project is built in its own Docker container and has no access to other builds or files produced by other builds. Containers run only with normal user privileges (no root). All files produced by the build are served over HTTPS (only). 

**Can version ranges be used with JitPack?**

Not at the moment. 

**How long is a build timeout?**

15 minutes

**Other questions**

Send them to jitpack at jitpack.io