# Release preparation

2026-09-06: Prepared a portable setup recipe from accepted framework `63446a28111a21a0cb7e8b5106c3614c898fc4b5`.
The release snapshot keeps functional code and title seed bytes, adds the bounded setup backport, and excludes private input/history.
Consulted the local release process, PSX-PUB-016, the accepted title handoff, and [Git orphan-branch documentation](https://git-scm.com/docs/git-checkout).
The shared archive gate now accepts only exact hashes for two intentional SDK path-example files; changed and relocated fixtures still fail.
Native CI and Windows package acceptance are pending.

2026-09-07: Native canary gates required the existing PSX-BUILD-024 C-linkage correction and the exact public recomp-ui be8ac1d portable tool text fix. The package now carries all four complete public dependency identities (PSX-PUB-027). No game runtime behavior or recipe settings changed in this update. Native build and package checks remain required.

2026-09-07: The Wipeout setup case finding also applies to this retained lowercase boot path. Actual preparation rejects sles_013.70 and succeeds for the ISO9660 entry SLES_013.70 with unchanged disc/program bytes. The portable boot path and generated filenames now use that exact case. No runtime setting or seed byte changed.

2026-10-01: Retargeted the kit from the European release (SLES-01370 and SLES-11370, SCPH-5552 BIOS) to the USA release (SLUS-00594 and SLUS-00776, SCPH-1001 BIOS). Alex decided that Metal Gear Solid ships as the USA version in pin H (PS1B-333).
The disc identities are those of the Redump dumps `Metal Gear Solid (USA) (Disc 1) (Rev 1)` and `Metal Gear Solid (USA) (Disc 2) (Rev 1)`.
Both discs boot the same program: `SLUS_005.94` and `SLUS_007.76` are byte-identical (651264 bytes, SHA-256 `615e136083336957ed0b9b3805145bf5bbb35f7a16c2f160dba8f17bb71cc640`, entry `0x8009B9B0`).
The ISO9660 entries are upper case and `SYSTEM.CNF` names them in lower case, as on the European disc, so the boot path and generated filenames keep the upper-case spelling.
The seed list is a new first-pass scan of the USA program (1672 seeds). The European seed list (76 seeds) does not apply to it and was removed.
The entries above this one describe the European build. The USA target has not been built or run.
