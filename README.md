Install Octave (macOS)
======================

### GitHub Action to install [GNU Octave][1] on macOS

Installs [GNU Octave][1] on macOS runners and sets the following environment
variables.
- `IS_MATLAB` set to 0
- `IS_OCTAVE` set to 1
- `ML_CMD` set to `octave-cli --no-gui --eval`
- `ML_PATHVAR` set to `OCTAVE_PATH`
- `OCTAVE_VER` set to the version of [Octave][1] installed

### Inputs / Outputs

None.

### Example Usage
```
    steps:
    - name: Install Octave
      uses: MATPOWER/action-install-octave-macos@v1

    - name: Octave ${{ env.OCTAVE_VER }} Installed
      run: $ML_CMD ver
```

[1]: https://octave.org
