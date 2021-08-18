Install Octave (macOS)
======================

### GitHub Action to install [GNU Octave][1] on macOS

Installs [GNU Octave][1] on macOS runners and sets the following environment
variables.
- `OCTAVE_VER` set to the version of [Octave][1] installed
- `IS_MATLAB` set to 0
- `IS_OCTAVE` set to 1
- `ML_NAME` set to `Octave`
- `ML_VER` set to same as `OCTAVE_VER`
- `ML_CMD` set to `octave-cli --no-gui --eval`
- `ML_PATHVAR` set to `OCTAVE_PATH`

### Inputs / Outputs

None.

### Example Usage
```
    steps:
    - name: Install Octave
      uses: MATPOWER/action-install-octave-macos@v1

    - name: Octave ${{ env.ML_VER }} Installed
      run: $ML_CMD ver
```

[1]: https://octave.org
