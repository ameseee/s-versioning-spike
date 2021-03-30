# Contributing to Savile

Please always following the standards in our [Contributing Guide](https://www.notion.so/turingschool/How-to-Contribute-1b88e17f755c491989e4b2bc84db93c7).

## Versioning

⁉️I would love to write a quick "what constitutes a new version blurb/expectation here, could use your help KK

Savile currently has a `beta` version released at `https://savile.turing.edu/css/versions/v-beta.css`. (this is a lie as of now, I am dream-writing) Any work that is merged into the `main` branch will not affect this version, as the URL points to a static file inside of `css/versions`. Files in that directory should never be changed except for their origination and the rare patch. 

⁉️RE the section below: I made up these naming conventions just so we have something but will happily change them! Your feedback is welcome!

When the team is ready to release a new version, follow these instructions:
- Checkout to a new branch following the naming convention `v[version-number]-release` (e.g. `v2-release`)
- Build the site. This can be done with `bundle exec jekyll build`, or, if you are running the local server with `bundle exec jekyll serve`, it will build for you.
- Locate the `_site/css/main.css` file and copy the contents to clipboard
- Create a new file under `css/versions`; name the file following the naming convention `v-[version-number].css`. Paste what is on your clipboard into this file
- Commit this new file with `git commit -m "Store v-[version-number] in versions directory"`
⁉️ Should we make a git tag here? If so, a naming convention?
- Push these changes up and make a PR

Once this PR is merged, two things will happen:
- The `main` branch will be updated with these changes (as you'd expect)
- Savile users can now choose to access this new version at `https://savile.turing.edu/css/versions/[version-file-name].css`.

### Patching Versions

[I would love to write a quick "what constitutes a _patch_ blurb/expectation here, could use your help KK]

If the team decides that a patch is necessary a specific version, follow these instructions:
[⁉️ If we are using git tags, is the branch part necessary? I'm a bit confused about how those work, but thinking that if we use tags this begining step may be changed/added to?]
- Fetch and checkout to the branch associated with the version
- Make desired changes
- Build the site
- Locate the `_site/css/main.css` file and copy the contents to clipboard
⁉️Does this next step sound right, or should they create a new file with a patch number - it used to be 2.0.0 but now it's 2.0.1 or something to that effect??
- Locate the file associated with the version inside of `css/versions` and paste what is on your clipboard into this file
- Commit this new file with `git commit -m "Patch v-[version-number]"`
⁉️ Again, if tagging - do we add a new tag for this patch at this point, I'd imagine?
- Push these changes up and make a PR