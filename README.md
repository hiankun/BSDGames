* The repo was copied from [vattam/BSDGames](https://github.com/vattam/BSDGames).

* Test environment: Lubuntu 18.04.

# If you want to build the whole package...

## Change some files

* Change all the `getline` to other name (e.g., `my_getline`) in files mentioned by error messages.
* For `boggle`:
  * It need a dictionary file to build. According to [this issue](https://github.com/vattam/BSDGames/issues/6#issuecomment-450537151),
    do the following to pass the `make` process:
    ```
    ln -s /usr/share/dict/words temp-dictionary
    ```
  * Another option is to add `boggle` into `bsd_games_cfg_no_build_dirs` of `config.params`.

## Installation

The installation is almost the same as the method given by INSTALL.
Only I don't install the games with root.

```
./configure
make (ignore the warnings)
make check (optional)
make install
```

## Some notes
If you wnat to play games in local folders, there are some paths have to be changed.
Take `atc` as the example, change the following paths in `atc/pathnames.h`:
```
//#define       _PATH_GAMES     "/usr/share/games/bsdgames/atc/"
//#define       _PATH_SCORE     "/var/games/bsdgames/atc_score"
#define _PATH_GAMES     "./games/"
#define _PATH_SCORE     "./atc_score"
```

---

I also added `tetris_test/` for test.
It is a stand-alone folder and the program can be build by using `bash build.sh`.
