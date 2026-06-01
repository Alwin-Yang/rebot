# rebot

A hands-on guide for **end-to-end imitation learning** with the [Seeed reBot](https://wiki.seeedstudio.com/rebot_b601_dm_getting_started/) arm — from hardware setup and teleoperation, through demonstration collection and policy training, to running a trained policy on the robot.

This repo walks you through the full pipeline:

1. **Set up the robot** — install SenseCraft, assemble, and calibrate the arm
2. **Collect demonstrations** — record human teleoperation trajectories
3. **Train a policy** — learn a behavior from your dataset (powered by [LeRobot](https://github.com/huggingface/lerobot))
4. **Deploy** — run the trained policy on reBot for closed-loop control

Third-party dependencies are vendored as Git submodules under `third-party/`:

- `third-party/reBot-DevArm` — hardware docs and assets
- `third-party/lerobot` — Hugging Face LeRobot

## Clone

Clone with submodules included:

```bash
git clone --recurse-submodules git@github.com:Alwin-Yang/rebot.git
```

If you already cloned the repo without submodules:

```bash
git submodule update --init --recursive
```

## Install SenseCraft

Download the latest package from the [SenseCraft Robotics download page](https://test-sensecraft-expose.seeed.cc/robotics/#download).

On Linux:

```bash
cd ~/Downloads
sudo dpkg -i SenseCraft-Robotics.deb
```

## Calibrate the robot

> **Note:** Complete robot assembly before calibration.

Follow the calibration guide in the [reBot B601 DM getting started wiki](https://wiki.seeedstudio.com/rebot_b601_dm_getting_started/#step-3-calibration-rebot-arm-and-getting-started).
