# Eye tracking for Alakazam

A plugin for [Alakazam](https://github.com/markspan/Alakazam): the EyeLink recording of the same session joined onto the EEG by EYE-EEG: the two clocks aligned through the triggers both received, the gaze and pupil signals added as channels and the tracker's saccades, fixations and blinks as events, with the synchronisation checked and recorded.

It was part of Alakazam until it became a plugin of its own, so that it can be
installed, upgraded and documented on its own.

## Manual

The manual is on this repository's pages:
<https://markspan.github.io/AlakazamEyetracking/>.

## Installing

In Alakazam, **Install plugins** on the Alakazam tab lists this repository:
select it and press **Install**. It installs the latest release. A zip from
the [releases](https://github.com/markspan/AlakazamEyetracking/releases), or one built with
`build`, installs the same way through **From a link**, and so does the link
to this repository. The tool appears on the Tools tab, as it did before.

It needs Alakazam V0.4.5.3 or newer, the first without `EyeTracking` built
in. Workspaces and templates made with the built-in tool open and
recalculate as before once the plugin is installed; Alakazam offers to
install it when one needs it.

## Building and testing

```matlab
build()                                    % dist/EyeTracking-<version>.zip
runtests('tests')                          % the tool's tests and the install
```

The tests need Alakazam's source: the folder in `ALAKAZAM_ROOT`, or the
Alakazam repository beside this one.

The join runs EYE-EEG (v1.01, pinned), which Alakazam downloads on first use, with consent. The tests tagged External need it, and skip without it; they never download it.

## Licence

GPL-3.0, as Alakazam.
