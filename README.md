# Daikin ONE Touch (Local) — Control4 driver

Local control of **Daikin ONE / ONE+** smart thermostats in **Control4**, over the thermostat's
**local API (UDP port 10444)** — **no cloud, no account, no subscription**. Free.

## Why
The usual ways to get a Daikin thermostat into Control4 lean on a cloud integration. This driver
talks straight to the thermostat **on your own LAN**, so it keeps working with the internet down
and doesn't depend on anyone's servers.

## Install
1. In **Composer Pro**: **Driver → Add or Update Driver…** and import `daikin_one_local.c4z`.
2. Add the driver (Comfort / Thermostat area) and set the thermostat's **Unit IP** in its properties.
3. Leave **Send Commands = "No – read only"** for a safe first test; confirm it reads correctly,
   then switch it to control.

## What it does
- Reads the thermostat **locally** (temperature, setpoint, mode, etc.).
- Optional local **control** (setpoint / mode) once you enable it.
- Fully local — never calls Daikin's cloud.

## Notes
- The driver is **encrypted** (the Lua runs on Control4 controllers only).
- Provided **free, as‑is, no warranty**. Not affiliated with or endorsed by Daikin or Control4 / Snap One.
