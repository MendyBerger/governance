# Proposal to Create webidl2wit

This document is a proposal to create webidl2wit as a formal Hosted Project under the auspices of the TSC of the Bytecode Alliance, as specified in the TSC’s charter.

Proposing the adoption of github.com/wasi-gfx/webidl2wit as a Bytecode Alliance hosted project.

Current Repository URL: https://github.com/wasi-gfx/webidl2wit.

Proposed Repository URL: https://github.com/bytecodealliance/webidl2wit (URL of the repository to be created within the Bytecode Alliance GitHub organization)

webidl2wit translates WebIDL to wit. It is used in wasi:webgpu proposal and in [browser.wit](https://github.com/MendyBerger/browser.wit).

This project includes both webidl2wit Rust library, and webidl2wit-cli.

## Requirements

### Alignment with the Bytecode Alliance Mission

> Projects must have alignment with [the Bytecode Alliance mission:](https://github.com/bytecodealliance/governance/blob/main/mission.md)
>
> > Our mission is to provide state-of-the-art foundations to develop runtime environments and language toolchains where security, efficiency, and modularity can all coexist across a wide range of devices and architectures. We enable innovation in compilers, runtimes, and tooling, focusing on fine-grained sandboxing, capabilities-based security, modularity, and standards such as WebAssembly and WASI.
>
> The Bytecode Alliance is a group with a specific mission, and we therefore will only sponsor projects that are in alignment with and further that mission. For example, project sponsorship is untenable if the project undermines sandboxing, security, or standardization efforts.

Given that webidl2wit is already used in wasi:webgpu, as well as in browser.wit - which is not wasi but uses wasm and the component-model - I think it would be a great fit for the BA

### Code Review

#### Description

> All projects must gate merging pull requests on code reviews that audit not only for style but also substance, such as whether security invariants are properly maintained by the new code.
>
> It is recommended, but not required, that hosted projects maintain a `CODEOWNERS` file and automatically assign reviewers as well.
>
> Code reviews have a demonstrable impact on the quality of source code by catching bugs early, determining the best possible implementation, and fostering trust within the community. Timely responses let contributors know that their work is valued and encourages further contribution.

This project will adopt code reviews going forward.

### Code of Conduct

> All Bytecode Alliance projects must:
>
> * link to the Bytecode Alliance's Code of Conduct documents from a `CODE_OF_CONDUCT.md` file in root of the repository, and
> * enforce the codes of conduct among the community and contributors, or escalate to [the Bytecode Alliance CoC Team](mailto:report@bytecodealliance.org), if needed.
>
> Having a code of conduct is crucial for creating a positive and respectful environment in any organization, community, or group. It serves as a set of guidelines that outline expected behavior and ethical standards for all members involved.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Continuous Integration Testing

> All projects must run continuous integration (CI) tests on all pull requests and merges. Key project features must be covered by CI.
>
> If any part of the CI gates on merging changes that is not reproducible by external contributors, then the project must make affordances to support those external contributors.
>
> Implementing CI offers several benefits to software projects, helping ensure correctness and quality, making it an essential practice for modern software development.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Contributor Documentation

> All projects must have a `CONTRIBUTING.md` document in the root of their repository. This document must provide, or link to another form of project-specific documentation that provides, high-quality contributor documentation.
>
> See ["How to build a `CONTRIBUTING.md`" by the Mozilla Science Lab](https://mozillascience.github.io/working-open-workshop/contributing/) for more details on what a high-quality `CONTRIBUTING.md` file looks like.
>
> A `CONTRIBUTING.md` serves as a guide for potential contributors, outlining the expectations for individuals who wish to contribute to the project. The Bytecode Alliance is a community-driven software foundation and documents like `CONTRIBUTING.md` are necessary for fostering community contributions.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Following the Bytecode Alliance Operational Principles

> All projects must follow [the Bytecode Alliance Operational Principles](https://github.com/bytecodealliance/governance/blob/main/operational-principles.md).
>
> In pursuing our mission and vision, the Bytecode Alliance follows a set of operational principles aimed at keeping us aligned on three key aspects: what we want to create, how we want to work together, and how we want to work with others.

The maintainers of this project are committed to the Bytecode Alliance Operational Principles.

### Licensing Compatible with the Bytecode Alliance

> All projects must be licensed under the Apache 2.0 license with an LLVM exception. Exemptions may be granted by the board.
>
> All projects must only use dependencies and third-party code licensed under one of the following open source licenses:
>
> * Apache-2.0 WITH LLVM-exception
> * Apache-2.0
> * BSD-2-Clause
> * BSD-3-Clause
> * ISC
> * MIT
> * MPL-2.0
> * OpenSSL
> * Unicode-DFS-2016
> * Zlib
>
> All dependencies and third-party code must be properly attributed.
>
> The source for all projects must be available to all members and must be available to all non-members under the same license.
>
> All projects must automatically ensure that licensing requirements of dependencies are met in CI.
>
> We strive to build an open community and a legally-compatible software ecosystem.

https://github.com/wasi-gfx/webidl2wit/blob/main/LICENSE

### README

> All hosted projects must have a `README.md` file in the root of the repository which begins with:
>
> * The project name and logo (if one exists)
> * A one-sentence description of the project
> * `<strong>A <a href="https://bytecodealliance.org/">Bytecode Alliance</a> hosted project</strong>`
>
> The most important information about the project should be "above the fold". Projects should identify themselves as Bytecode Alliance projects so that, with time, people associate the Bytecode Alliance with quality projects that they can rely on.

[github.com/wasi-gfx/webidl2wit/blob/main/README.md](https://github.com/wasi-gfx/webidl2wit/blob/main/README.md) has the project name and a brief description. We'll add the BA link once accepted to the BA.

### Release Process

> Documentation of a release process that any project maintainer may execute to create a new release version of the software.
>
> Multiple people must have permissions to publish releases. A github team must have access to publish packages and package ownership on the associated package repository when possible. For example a Rust project may have multiple owners on crates.io.
>
> Projects and their releases shouldn't be tied to any single user's machine or keys to ensure continuity of the project. A project isn't an open, community project if only one person can publish releases.
>
> Automation makes fewer mistakes than humans, and getting releases right is critical, since only releases are typically used downstream, not random commits from `main`.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Security Process

> All projects must have a documented security process for reporting and disclosing vulnerabilities, managing patches that fix vulnerabilities, and announcing and making available security releases. Furthermore, projects must actually follow their documented processes.
>
> It is recommended that request Common Vulnerability and Exposure (CVE) numbers for discovered vulnerabilities and report the CVE when disclosing the vulnerability.
>
> A tool like [dependabot](https://github.com/dependabot) may suffice for hosted projects. Dependabot should be used for security updates only, and not apply all updates indiscriminantly. Updating dependencies should otherwise be done with intention (never automatically). Automatic creation of pull requests is acceptable, but manual review is required to prevent supply chain attacks.
>
> Bytecode Alliance projects must be a secure foundation for others to build upon. Transparency and a managed security release process is key to being this foundation.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Semantic Versioning

> All projects must follow either standard semantic versioning or their ecosystem's local-dialect of semantic versioning (for example, Rust and `cargo`'s interpretation of semantic versioning slightly differs from the standard, but is acceptable for Rust Bytecode Alliance projects).
>
> A clear versioning scheme is necessary for end-users. We desire consistency across projects and so the Bytecode Alliance has adopted semantic versioning as a required best practice.

We currently have only one release, but we sure plan to stick to samantic versioning, and have that built into our release CI.

### Secrets Management

> GitHub organization and repository level secrets should be used. Secrets must not be hard coded in source.
>
> For secrets like passwords for the project's associated social media account, these should be stored in the password service paid for by the Bytecode Alliance. Contact the TSC for access and ability to manage a given secret.
>
> Secure secret management is a requirement for a secure project. Additionally, projects and their associated accounts shouldn't be tied to any single user's machine or keys to ensure continuity of the project. A project isn't an open, community project if only one person can access its accounts.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Supply Chain Security

> All projects must follow a well-documented process for updating dependencies and auditing them for malicious supply-chain attacks.
>
> When applicable, projects should:
>
> * Integrate auditing tools in CI (such as `cargo vet`)
> * Use code review and static analysis tools on dependencies
>
> Finally, projects must document and follow their process for responding to upstream vulnerabilities in dependencies.
>
> Our mission of developing runtime environments and language toolchains where security, efficiency, and modularity can all coexist necessarily means that we have performed our due dilligence to mitigate software supply chain attacks.

TODO: argument that this requirement is fulfilled and supporting evidence (such as links to code, documentation, issues, and pull requests)

### Sustainable Contributor Base

> All projects must have regular contributions from multiple contributors.
>
> It is recommended that hosted projects additionally have contributors affiliated with at least two different Bytecode Alliance organizations and that the project's leadership has representation from at least two different Bytecode Alliance organizations.
>
> There must not be any private information necessary to fully contribute to the project.
>
> A project is not considered healthy with only one contributor. An open, community project requires input from multiple stakeholders and does not rely on a single person.
>
> The TSC may waive the above contributor base requirements under certain conditions. In particular, the TSC may decide to adopt crucial upstream dependencies of existing Bytecode Alliance projects that are otherwise effectively unmaintained or only have a single maintainer.

webidl2wit is maintained by @MendyBerger and @vados-cosmonic. See https://github.com/wasi-gfx/webidl2wit/graphs/contributors.

### Version Control

> All projects must be hosted on [the Bytecode Alliance Organization](github.com/bytecodealliance) on GitHub.
>
> Access controls are managed via the Bytecode Alliance organization on GitHub. This allows for continuity of the project when hosted in one place. Finally, this is the only way to reasonable manage the projects within the organization.

We are willing to move the project to github.com/bytecodealliance/webidl2wit.

## Recommendations

### Changelog

> It is recommended that hosted projects highlight key additions, breaking changes, security fixes, and otherwise noteworthy changes in a changelog.
>
> See [keepachangelog.com](https://keepachangelog.com/en/1.1.0/) for a recommended approach.
>
> We are building an ecosystem that developers can depend on, and one small part of that is communicating important changes downstream.

We have changelogs for both [webidl2wit](https://github.com/wasi-gfx/webidl2wit/blob/main/crates/webidl2wit/CHANGELOG.md) and [webidl2wit-cli](https://github.com/wasi-gfx/webidl2wit/blob/main/crates/webidl2wit-cli/CHANGELOG.md
), though the both can use some love. 

### Continuous Fuzzing

> Not all projects will necessarily benefit from fuzzing, for example benchmark suites. The TSC may choose lift this requirement for a particular project.
>
> It is recommended that hosted projects have 24/7, round the clock, continuous fuzzing. The fuzzing should exercise significant amounts of the code base and test the project's most important properties, such as sandboxing. Bugs and vulnerabilities discovered via fuzzing should be addressed promptly.
>
> Part of our open-source and open contribution model, the corpus and setup for running fuzzing should be open-sourced as part of the project.
>
> Faults discovered via fuzzing must be reported privately to the project's core team so that the project's security vulnerability process can be followed properly, if necessary. For example, fuzzing infrastructure must not automatically open public issues for any fault that is discovered.
>
> Continuous fuzzing is a valuable practice for projects, due to its significant benefits in improving security and reliability. Within the Bytecode Alliance, we host projects that provide a sandbox. The fidelity of these sandboxes must be battle-tested via a number of methodologies including automated fuzzing.

We don't have continuous fuzzing.

### End-User Documentation

> We abide by [the OpenSSF requirements for documentation](https://bestpractices.coreinfrastructure.org/en):
>
> > The documentation of an external interface explains to an end-user or developer how to use it. This would include its application program interface (API) if the software has one. If it is a library, document the major classes/types and methods/functions that can be called. If it is a web application, define its URL interface (often its REST interface). If it is a command-line interface, document the parameters and options it supports. In many cases it's best if most of this documentation is automatically generated, so that this documentation stays synchronized with the software as it changes, but this isn't required. The project MAY use hypertext links to non-project material as documentation. Documentation MAY be automatically generated (where practical this is often the best way to do so).
>
> Furthermore, we identify a few different types of (sometimes overlapping) documentation:
>
> * **API documentation**: Documentation for each type, method, function, and module in a library.
> * **Architectural overviews**: High-level documentation about the architecture of the project and how it works from a 1000-foot view that helps endusers take advantage of the project in the best way possible and helps onboard new contributors.
> * **Examples**: Code examples that show off how to use the project as a whole or particular features it supports.
> * **Guides and tutorials**: Long-form prose, with code samples interspersed, that shows how to accomplish a task using the project.
>
> API and CLI flag documentation is required for hosted projects; all other types are recommended.
>
> Documentation is necessary for end-users to productively use the project; source code comments are not sufficient.

TODO: discussion of this recommendation and any supporting evidence (such as links to code, documentation, issues, and pull requests)

### Issue Triage Process

> Hosted projects must use an issue tracker for tracking individual issues.
>
> It is recommended that hosted projects should additionally have a documented process for expeditiously triaging incoming issues and pull requests, and follow that process. Contributors should get prompt responses to their issues and pull requests, even if a response is not an immediate fix or review.
>
> For a successful community-driven project, expedient communication within issues and PRs encourages further collaboration and contribution.

We don't have an issue triage process.

### Leverage the Bytecode Alliance RFC Process

> A request for comments (RFC) is a technique for soliciting the community and contributors for feedback on proposed major changes and decisions.
>
> It is recommended that hosted projects follow [the Bytecode Alliance RFC process](https://github.com/bytecodealliance/rfcs/blob/main/accepted/rfc-process.md) for changes that significantly affect project stakeholders or contributors. The RFCs repo describes [when an RFC is needed](https://github.com/bytecodealliance/rfcs/#when-is-an-rfc-needed) in more detail:
>
> > Many changes to Bytecode Alliance projects can and should happen through every-day GitHub processes: issues and pull requests. An RFC is warranted when:
> >
> > * The work involves changes that will significantly affect stakeholders or project contributors. Each project may provide more specific guidance. Examples include:
> >     * Major architectural changes
> >     * Major new features
> >     * Simple changes that have significant downstream impact
> >     * Changes that could affect guarantees or level of support, e.g. removing support for a target platform
> >     * Changes that could affect mission alignment, e.g. by changing properties of the security model
> > * The work is substantial and you want to get early feedback on your approach.
>
> This is a best practice for aligning contributors, the community, and downstream projects' needs with proposed technical implementations.

TODO: discussion of this recommendation and any supporting evidence (such as links to code, documentation, issues, and pull requests)

### Production Use

> It is recommended that hosted projects have demonstrated use in production by at least three independent organizations which are, in the TSC's judgement, of adequate quality and scope.
>
> It is recommended that projects track production usage by organizations in an `ADOPTERS.md` at the root of the project, for example see [`ADOPTERS.md`](https://github.com/bytecodealliance/wasmtime/blob/main/ADOPTERS.md) in Wasmtime.
>
> Projects should demonstrate that they are practical, useful, and reliable enough to use in production.

TODO: discussion of this recommendation and any supporting evidence (such as links to code, documentation, issues, and pull requests)

### Public Project Meetings and Notes

> It is recommended that hosted projects hold regular and public project meetings. Meeting times and frequency should be advertised publicly, for example in the project's `CONTRIBUTING.md`. To avoid spam and "Zoom bombing", the video conferencing link need not be public, but should be available upon request.
>
> Agendas for upcoming meetings and notes from past meetings should be published publicly. The notes should be in the `bytecodealliance/meetings` repository.
>
> Public meetings encourage open communication, collaboration, and engagement within the project's community. Notes allow community members who were not present to remain aligned and can document any decisions made during the meeting.

We don't have project meetings.

### Sanitizers and Code Analysis

> Static and dynamic code analysis tools (such as `valgrind` or `miri`) where applicable are recommended to be used by hosted projects.
>
> It is recommended that hosted projects with non-trivial amounts of unsafe code (e.g. `unsafe` in Rust or any C/C++)  run tests and fuzzers with the relevant sanitizers: Address Sanitizer, Memory Sanitizer, Thread Sanitizer, etc.
>
> Automated code analysis is key to meeting our mission of developing runtime environments and language toolchains where security, efficiency, and modularity can all coexist.

TODO: discussion of this recommendation and any supporting evidence (such as links to code, documentation, issues, and pull requests)
