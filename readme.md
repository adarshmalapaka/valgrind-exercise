# C++ Boilerplate
[![Build Status](https://travis-ci.org/dpiet/cpp-boilerplate.svg?branch=master)](https://travis-ci.org/dpiet/cpp-boilerplate)
[![Coverage Status](https://coveralls.io/repos/github/dpiet/cpp-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/dpiet/cpp-boilerplate?branch=master)
---

## Overview 

The codes in the ```valgrind_branch``` contained memory leak and data uninitialization errors which were observed using Valgrind and rectified. 

## Running the Program
```
git clone https://github.com/adarshmalapaka/valgrind-exercise
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run program: ./app/shell-app
```

### Valgrind

```
sudo apt install valgrind
cd build
valgrind --leak-check=full -v ./app/shell-app >& ../results/valgrind_rectified_result.txt
```

### KCachegrind

```
sudo apt-get install -y kcachegrind
cd build
valgrind --tool=callgrind  ./app/shell-app
kcachegrind
```

Open the ```callgrind.out.xxxx``` file in the GUI.