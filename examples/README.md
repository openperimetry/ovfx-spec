# OVFX example documents

Each file in this directory is a complete, conformant OVFX document. They are validated against the schema in CI.

| File                                                       | Test type | Eye    | Notes                                                    |
| ---------------------------------------------------------- | --------- | ------ | -------------------------------------------------------- |
| [`kinetic-goldmann.ovfx.json`](kinetic-goldmann.ovfx.json) | kinetic   | right  | Full five-isopter Goldmann test, with RT compensation.   |
| [`static-perimetry.ovfx.json`](static-perimetry.ovfx.json) | static    | left   | Static grid sample with one missed point.                |
| [`ring-test.ovfx.json`](ring-test.ovfx.json)               | ring      | right  | Eight-sector ring test with two stimulus levels.         |
| [`vr-phone-headset.ovfx.json`](vr-phone-headset.ovfx.json) | kinetic   | right  | Phone in a headset (`vr` + `screen`), points with the fixation moved (`extendedPass`, `device*`) and two re-checks (`startEccentricityDeg`, `repeat`). |

To validate locally:

```bash
cd tools/validate-cli
npm install
node index.js ../../examples/*.ovfx.json
```
