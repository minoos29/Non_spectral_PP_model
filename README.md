# Primary Production practical

This repository contains a practical exercise of Primary Production developed by Bob Brewin at the University of Exeter (r.brewin@exeter.ac.uk).

Launch the practical by clicking the logo below Hello

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/PrimaryProduction/Non_spectral_PP_model/HEAD)

## Contents

| File | Description |
|------|-------------|
| `TPFS_PP_Practical.ipynb` | The practical notebook |
| `AQUA_MODIS.20230604.L3m.DAY.CHL.chlor_a.9km.NRT.nc` | MODIS-Aqua daily chlorophyll-a (9 km, 4 June 2023) |
| `AQUA_MODIS.20230604.L3m.DAY.PAR.par.9km.NRT.nc` | MODIS-Aqua daily PAR (9 km, 4 June 2023) |
| `requirements.txt` | Python packages needed by the notebook |

## Running the practical on WEkEO

Binder is the quickest way to try the notebook. It is also slow to start and sessions disappear when you close the tab. If you want a stable environment where your work is saved between sessions, run the notebook on the WEkEO JupyterHub instead.

### What is WEkEO?

[WEkEO](https://www.wekeo.eu) is one of the European Union's Copernicus DIAS platforms (Data and Information Access Services). It gives a single point of access to Copernicus satellite and model data together with cloud computing resources to analyse them. WEkEO is run jointly by EUMETSAT, ECMWF, Mercator Ocean International and the European Environment Agency (EEA). 

For users, the most useful part for this practical is the WEkEO JupyterHub. It is a free, browser-based JupyterLab environment with a ready-made Python setup. Everything runs on WEkEO's servers, so you do not need to install anything on your own computer. All you need is a free WEkEO account. The JupyterHub also has a `public` folder with many tutorial notebooks on ocean, atmosphere, climate and land data, which is a good place to continue after this practical.

### Step 1. Create a WEkEO account

1. Go to the registration page at <https://wekeo.copernicus.eu/register> (or open <https://www.wekeo.eu> and click **Register**).
2. Fill in the form with your name, email address, a username and a password, and accept the terms and conditions.
3. Check your inbox for the confirmation email and click the link to activate the account.

Registration and JupyterHub access are free. Do this before the workshop, since the confirmation email can take a little while to arrive.

### Step 2. Start a JupyterHub server

1. Sign in at <https://wekeo.copernicus.eu/my-wekeo>. This takes you to your MyWEkEO dashboard.
2. Click **Open** next to **WEkEO Workspace** (the JupyterHub).
3. Choose a server option. The standard CPU server (Earth Observation Tools) is enough for this practical. A GPU server is not needed.
4. Click **Start**. The server can take a few minutes to launch. When it is ready, JupyterLab opens in your browser.

### Step 3. Copy this repository into your workspace

1. In JupyterLab, open a terminal via **File > New > Terminal**.
2. Clone the repository into your home folder:

   ```bash
   git clone https://github.com/PrimaryProduction/Non_spectral_PP_model.git
   ```

3. A folder called `Non_spectral_PP_model` now appears in the file browser on the left. It contains the notebook and the two MODIS data files.

### Step 4. Install the required packages

Most of the packages in `requirements.txt` (numpy, pandas, matplotlib, scipy, netCDF4, cartopy) are already available on WEkEO. A few smaller ones, such as `julian` and `colour`, may be missing. In the same terminal, run

```bash
cd Non_spectral_PP_model
pip install --user -r requirements.txt
```

Packages that are already installed are skipped.

### Step 5. Run the notebook

1. Double-click `TPFS_PP_Practical.ipynb` in the file browser to open it.
2. If you are asked to pick a kernel, choose the default Python 3 kernel.
3. If you installed packages in Step 4 after opening the notebook, restart the kernel with **Kernel > Restart Kernel** so they are picked up.
4. Run the cells from top to bottom with **Shift + Enter**.

### Good to know

- Your files stay in your WEkEO workspace between sessions, so you can stop and come back later. Files are deleted if the account is inactive for five months.
- When you are done, stop your server with **File > Hub Control Panel > Stop My Server**. This frees up resources for other users.
- To get the latest version of the practical later, open a terminal and run `git pull` inside the `Non_spectral_PP_model` folder.
- Help is available in the [WEkEO Help Center](https://help.wekeo.eu) and from support@wekeo.eu.
