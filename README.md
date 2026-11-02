# carla-autoware-maps

Autoware maps (Lanelet2 + point cloud) for the CARLA 0.9 towns, as converted by TUM's
[CARLA-Autoware-Bridge](https://github.com/TUMFTM/Carla-Autoware-Bridge) project
(Kaljavesi et al., Technical University of Munich, 2024). This repository is a mirror: TUM's
own download links (LRZ Sync+Share) no longer work, and
[scenario-world-bridge](https://github.com/NEWSLabNTU/scenario-world-bridge) and its users
need the pack.

## Releases

| Release | Asset | What it is |
|---|---|---|
| `tum-2024-06` | `carla-autoware-bridge.zip` (313 MB) | TUM's pack exactly as they published it: Town01, Town02, Town03, Town05, Town10, each with `lanelet2_map.osm`, `pointcloud_map.pcd`, `map_config.yaml`, `map_projector_info.yaml` and `LICENSE.md` |

SHA-256 of `carla-autoware-bridge.zip`:

```
6e582242198ae50aa1d1fd410b53609c8b7ecfc6b9696294c498646783ed4838
```

The files are unmodified. scenario-world-bridge's `scripts/download_maps.sh` downloads this
asset, checks the checksum and then repairs, in its own copy, what Autoware and
scenario_simulator_v2 need fixed (traffic-light tags, lanelet subtypes, local coordinates,
turn directions, speed limits, ...); see its
[Getting started on CARLA](https://github.com/NEWSLabNTU/scenario-world-bridge/blob/main/docs/getting-started/carla.md).

## License

The maps are TUM's work, under the GNU Lesser General Public License v3.0
([LICENSE.md](LICENSE.md), the copy that ships in each town directory). Copyright 2024
Gemb Kaljavesi, Technical University of Munich. If you use them in research, cite TUM's paper:
G. Kaljavesi, T. Kerbl, T. Betz, K. Mitkovskii, F. Diermeyer, "CARLA-Autoware-Bridge:
Facilitating Autonomous Driving Research with a Unified Framework for Simulation and Module
Development", IEEE IV 2024 ([arXiv:2402.11239](https://arxiv.org/abs/2402.11239)).
