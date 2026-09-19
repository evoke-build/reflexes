# Reflexes

The first-party collection: one directory per reflex, `reflex.toml` plus the file `run` names
([design](../docs/design.md#reflex)). Until [step 12](../docs/roadmap.md#12-reflexes) writes the bodies, these are seed
manifests: the eval spike's material and the spec's fixtures. Where `run` is an argv, it is macOS's.

| Reflex                             | Effect      | Run  | Exercises                                    | Near  |
| :--------------------------------- | :---------- | :--- | :------------------------------------------- | :---- |
| [timer](timer/reflex.toml)         | write       | file | `duration`; optional `quoted`                | awake |
| [awake](awake/reflex.toml)         | write       | file | optional `duration`; unstated asserted       | timer |
| [volume](volume/reflex.toml)       | write       | file | `number` with `range`                        |       |
| [wifi](wifi/reflex.toml)           | write       | argv | `options` into argv                          |       |
| [lock](lock/reflex.toml)           | write       | file | no arguments                                 | power |
| [power](power/reflex.toml)         | destructive | file | `options`; effect stated                     | lock  |
| [screenshot](screenshot/reflex.toml) | write     | file | optional `options`; `flag`                   |       |
| [note](note/reflex.toml)           | write       | file | `quoted`; `[config]`                         |       |
| [open](open/reflex.toml)           | read        | argv | `vocab` into argv                            | visit |
| [visit](visit/reflex.toml)         | read        | file | `vocab`; `flag`                              | open  |
| [download](download/reflex.toml)   | write       | file | `url`; optional `vocab`, shared with `open`  |       |
| [mail](mail/reflex.toml)           | read        | file | `email`; optional `quoted`                   |       |
| [trash](trash/reflex.toml)         | destructive | argv | no arguments; effect absent                  |       |
