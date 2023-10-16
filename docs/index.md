# SIG/FastTrack Wiki

## A Package Bazaar, not a Package Cathedral

FastTrack, as an ode to a past CentOS repository of a similar name, is a SIG that attempts to provide:

  * Fixes, customizations, upgrades, and improvements to existing Rocky packages that the community would like to see
  * Backports of patches that may not be released by our upstreams (RHEL, CentOS Stream, or even Fedora) to address bugs or functionality
  * New original packages for Rocky.  It's possible new ones could eventually make it into CentOS Stream or EPEL.
  * Newer major versions of software that override the base Rocky repositories - even versions so new they will likely never land in RHEL, CentOS Stream, or EPEL


## Philosophy

The goal is to have a place in the Rocky project where experimental new packages and updates to existing ones can be published.  Philosophically, this SIG should be wide open to contributions, with much less rigor or vetting than repositories such as EPEL. Newer versions of existing Rocky Linux packages, as well as brand new packages are both welcome.  **We don't need reasons to add a package, we need reasons to *not* add it.


Having said that, we can't have absolute anarchy. There must be some kind of a guideline to what can and cannot be accepted.

### Reasons for FastTrack Package Rejection:

- **Broken dependencies:**  `dnf repoclosure` must succeed on publication.  If some packages are not installable under default Rocky Linux, we cannot include the package until that's fixed
- **Malicious or severe security risk:**  We should not publish anything that presents a severe security risk to the user (think remotely-exploitable-by-default code).
- **Changes a core package in a questionable way:** Related to the security risk issue.  We cannot override `openssl` or `glibc` with questionable behavior or API updates.  "Core" is in the eye of the beholder, but generally we want FastTrack users to continue using the solid Rocky Linux base.
- **We don't have permssion to redistribute:** Self-explanatory.  Contributions don't necessarily have to be 100% open source, but the Rocky project cannot and will not host copyrighted, non-redistributable content.
- **It already exists in EPEL, RPMFusion, or another 3rd-party repo**:  The intention of this SIG is to provide as much "new and cool" stuff to Rocky Linux users as possible. If people can already get software from one of the popular 3rd-party repos, that's probably the best place to go.  An exception to this is when dependencies are needed that already exist in another repo, that are needed to build the new package we want.
- **Package clearly belongs in another SIG:** The goal of this SIG is to be a "catchall" for desirable new packages or updates. However, many times a package clearly doesn't belong in FastTrack, but in another SIG already set up for that purpose. Enhanced kernels should probably go in SIG/Kernel, embedded or single-board specific packages should go in SIG/AltArch, etc.


Outside of these guidelines, package contributions should always be welcome!


## Links

- **SIG-FastTrack Wiki:**  [https://sig-fasttrack.rocky.page/](https://sig-fasttrack.rocky.page/)
- **MatterMost Chat Channel:** [https://chat.rockylinux.org/rocky-linux/channels/sig-fasttrack](https://chat.rockylinux.org/rocky-linux/channels/sig-fasttrack)
- **FastTrack Git Group:** [https://git.resf.org/sig_fasttrack/](https://git.resf.org/sig_fasttrack/)  (New package requests can be in meta/, wiki source under wiki/ )
- **FastTrack Package Sources:** [https://git.rockylinux.org/sig/fasttrack/](https://git.rockylinux.org/sig/fasttrack/)
- **Peridot RPM Build System:** [https://peridot.build.resf.org/](https://peridot.build.resf.org/)


## Responsibilities

## Meetings / Communications

## Members

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
