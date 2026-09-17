# Throw The Switch Design and Development Process

Hi. Thanks for using ThrowTheSwitch.org's tools. We're the makers of Ceedling, CMock, and Unity Test, 
among other useful projects.

We understand that our tools are used in high-reliability industries, and so we've collected these 
resources together to help you with certification processes. If there are areas that we can improve
or elaborate on, please feel free to make recommendations.

## Who Are We?

We are a collection of Open Source projects. As such, we have the advantage of many eyes on our projects,
but also the challenge of varied skills and thoroughness. ThrowTheSwitch.org is partnered with
ThingamaByte, LLC, which provides support and well as additional validation of these projects. Together, 
we have developed this process to increase the quality of our projects, while taking advantage of the 
wide user base. 

We maintain a code of conduct because we believe that the best software is created when people can 
respect and trust one another. Also, because it's the right thing to do.

Refer to our [Code of Conduct](CODE_OF_CONDUCT.md)

## Change Requests

Our projects are hosted on Github. We take advantage of Github Issues to track desired features and 
any issues that are identified. Issues that are identified through other means (the forums, our contact
forms, direct email, support contracts, etc) are also added as issues by the maintainers.

Refer to our [Contribution Documentation](CONTRIBUTING.md)

Issues that are submitted are traiged for severity. Features and bugfixes are assigned to an upcoming
release in Github Projects, where they can be tracked. Where necessary, we request additional information
from reporters for reproducibility.

Often issues come with community Pull Requests with their own solutions. Each PR is evaluated by at least
one core maintainer. 

## Acceptance

Both community-submitted PR's and PR's submitted by maintainers follow the same acceptance criteria. 
Self-tests run as continuous integration on Github Actions. To be accepted, a PR must
pass all the tests and fulfill the checklist criteria. Whenever possible, additional tests are 
added to capture the discovered issue or support the new features. If the original author isn't available 
to perform necessary updates / improvements, PR can be redirected to another branch. Issues can then 
be addressed before performing. 

Refer to our [Pull Request Checklist](PullRequestChecklist.md)

Refer to our [Coding Standard](ThrowTheSwitchCodingStandard.md)

Each project maintains a changelog, a list of release notes and breaking changes. Each is a document 
maintained in the source repository itself. These help to enable tracking of changes by users from 
release to release.

 - [Ceedling Breaking Changes](CeedlingBreakingChanges.md)
 - [Ceedling Changelog](CeedlingChangelog.md)
 - ~~[Ceedling Known Issues](CeedlingKnownIssues.md)~~
 - [Ceedling Release Notes](CeedlingReleaseNotes.md)

 - ~~[CMock Breaking Changes](CMockBreakingChanges.md)~~
 - [CMock Changelog](CMockChangelog.md)
 - [CMock Known Issues](CMockKnownIssues.md)
 - ~~[CMock Release Notes](CMockReleaseNotes.md)~~

 - ~~[Unity Breaking Changes](UnityBreakingChanges.md)~~
 - [Unity Changelog](UnityChangelog.md)
 - [Unity Known Issues](UnityKnownIssues.md)
 - ~~[Unity Release Notes](UnityReleaseNotes.md)~~

## Validation

Each tool has multiple layers of validation, all of which are configured to run in continuous integration. 
All options are also available for users to run on their local hardware for validation with the rest of
their toolchain, with the exception of ThingamaByte's private collection of projects. 

- Unit Tests to validate key modules of code
- System Tests to validate overall functionality and protect against regression issues
- Style validation
- Static analysis of C code (not yet implemented)
- A public collection of example projects with expected results that new releases can be tested against.
- A private collection of example projects (maintained by ThingamaByte, LLC) to further protect again regression issues.

## Release Process

Official releases are made using the Github Release tools. The gem and snapshots are posted, along with the updated
documentation (including release notes, breaking changes, etc as described earlier). Official releases have passed all
self-tests on the primary targets. We're expanding our list of officially supported targets to better capture these needs.

Preview Releases are generated with each successful CI build. These are posted to allow the community to see
upcoming changes, validate changes on their own systems before adopting, etc. A reasonable backlog of preview releases
is maintained, but this list is frequently culled in order to minimize noise and overhead.

The official release gets a tag made in git, allowing anyone to access it at any point. Official releases are kept live on 
Github, allowing teams to access them at any time, even years after the release. Each project's release also includes a 
downloadable snapshot of the entire project, allowing a team to capture their own copy.

## Security

Our tools are made to run within development environments. As such, they have low-level access to anything
that the rest of the toolchain has access to. As they are local scripts without a network interface themselves,
any security concerns are more a factor of the environment they're running from than the tools themselves. Still,
we do our best to develop with responsible practices and address security issues as they arise. 

Refer to our [Security Processes](SECURITY.md)

## License and Guarantees

While we put significant effort into the quality of these projects, as stated in our license, these tools are
provided AS-IS, without warranty. If you DO run into issues, we'd appreciate your feedback, reports, or even
solutions via the processes described above! Together, we can raise the quality of software!

Refer to our [License](LICENSE)
