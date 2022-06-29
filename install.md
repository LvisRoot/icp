# ICP Sim(3) examples installation instructions

## install required packages
```
sudo apt-get install libfmt-dev
sudo apt-get install libgoogle-glog-dev
```

## Compile & Install Sphous dependancies
```
cd [repos_path]
git clone git@github.com:strasdat/Sophus.git
chmod +x Sophus/scripts/install_linux_deps.sh
sudo Sophus/scripts/install_linux_deps.sh
cd Sophus
mkdir build
cd build
cmake ..
make -j4
sudo make install
```

## Compile & Install icp Sim3
```
cd [repos_path]
git clone git@github.com:arntanguy/icp.git
cd icp
mkdir build
cd build
cmake .. -DENABLE_EXAMPLES=ON
make -j4
sudo make install
```

### run example
```
src/examples/icp_step_by_step
```
