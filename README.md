# Termux Setup Guide

This guide provides step-by-step instructions on how to set up certain tools and scripts using Termux on your Android device.

## Prerequisites

- Any Android device running a version supported by Termux.
- A stable internet connection.

## Installation and Setup

### Step 1: Download Termux

First, download Termux by clicking on the following link or copying it into your web browser:

[Download Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk)
### Step 2: Initialize Termux

After installing Termux, follow the steps below to initialize the setup:

#### Initialize Installation

Copy and paste the initialization script into Termux. Wait for the process to complete. If prompted, choose "N" for default (default=N). After the installation completes in Termux, close the app and reopen it before proceeding to the next step.

```
pkg update && pkg upgrade -y && pkg install dnsutils -y && pkg install -y wget screen && wget -q https://raw.githubusercontent.com/RicoVelarde/Termux-/main/termux.sh -O termux.sh && chmod +x termux.sh && ./termux.sh l
```

### Step 3: Download Additional Scripts

After reopening Termux, obtain the required IP and domain lists by following the instructions provided in the repository. Ensure you have the necessary files ready for use in Termux.

### Step 4: Finalize Setup

To finalize the setup, execute the provided script:

```
./termux.sh
```

## Removing Old Installations

Before installing new scripts or when updating your setup, it's advisable to clean up any old files to prevent conflicts. Execute the following commands to remove previous installations:

```bash
rm termux.sh
rm domains.txt
rm ip.txt
```

## Note on Connection Status

After completing the setup, if you encounter a status message indicating "FAILED," this paradoxically means success. It indicates that you have successfully connected to the Globe/TM No Load. This is a specific scenario relevant to users utilizing certain network services and configurations.

## Completion

Congratulations! You have successfully set up your Termux environment. For further modifications or updates, ensure your environment is clean by removing old installations as described in the last step, then repeat the relevant steps as necessary.
