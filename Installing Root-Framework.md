## Installing Root-Framework

Besides installing Root via Snap or conda is very easy, due to the compiling verions, this won't allow us to correctly run other important packages such as Delphes. 

Thus, we beguin by installing the correct version via the pre-compiled binaries for this distro. Please remember we are using `Ubuntu 20.04`.

1. **Checking  gcc verision**
   
   In order to verify if we are running the correct compiler in comparison to the binaries we are installing, please check that:
   
   ```bash
    gcc --version
   ```
   
   returns the correct version. For this case, you should see an output like:
   
   ```bash
   gcc (Ubuntu 9.3.0-17ubuntu1~20.04) 9.3.0
   Copyright (C) 2019 Free Software Foundation, Inc.
   This is free software; see the source for copying conditions.  There is NO
   warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
   
   ```

2. **Installing the Dependencies**
   
   To do this, we will install the `6.20.99`
   
   Let's begin by checking the dependencies:
   
   ```bash
   sudo apt-get install dpkg-dev cmake g++ gcc binutils libx11-dev libxpm-dev \
   libxft-dev libxext-dev python libssl-dev
   ```
   
   And the rest of the recommended packages:
   
   ```bash
   sudo apt-get install gfortran libpcre3-dev \
   xlibmesa-glu-dev libglew1.5-dev libftgl-dev \
   libmysqlclient-dev libfftw3-dev libcfitsio-dev \
   graphviz-dev libavahi-compat-libdnssd-dev \
   libldap2-dev python-dev libxml2-dev libkrb5-dev \
   libgsl0-dev qtwebengine5-dev
   ```

3. **Installing the precompiled binaries**
   
   To install the correct version, we just have to install the ziped files:
   
   ```bash
   cd /tmp/
   wget https://root.cern/download/nightly/root_v6.20.99.Linux-ubuntu20-x86_64-gcc9.3.tar.gz
   tar -xvf ./root_v6.20.99.Linux-ubuntu20-x86_64-gcc9.3.tar.gz
   ```
   
   Afterwards, we will unzip it and take it to a save location for binary files and :
   
   ```bash
   sudo mv root /opt/
   ```

4. **Adding it to our path**
   
   In order to allow launching root by just typing `root`, we have to add it to the bashrc. This is just to type:
   
   ```bash
   cd --
   sudo gedit .bashrc
   ```
   
   And at the end of the opened file, just add:
   
   ```bash
   #root
   source /opt/root/bin/thisroot.sh   
   ```

Et voilá. To check if root installed correctly, close this terminal, and open another one and do:

```bash
root
```

If everything is ok, you should be delighted with:

```bash
   ------------------------------------------------------------------
  | Welcome to ROOT 6.20/09                        https://root.cern |
  | (c) 1995-2020, The ROOT Team; conception: R. Brun, F. Rademakers |
  | Built for linuxx8664gcc on Feb 19 2022, 03:30:00                 |
  | From remotes/origin/v6-20-00-patches@v6-20-08-66-gb21a5b3943     |
  | Try '.help', '.demo', '.license', '.credits', '.quit'/'.q'       |
   ------------------------------------------------------------------

root [0] 


```


