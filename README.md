# testnet-flooki
for flooki testnet
sudo apt update -y

sudo apt upgrade -y

sudo apt install build-essential -y

sudo apt install libssl-dev pkg-config libclang-dev -y

curl https://sh.rustup.rs -sSf > RUSTUP.sh
sh RUSTUP.sh -y
rm RUSTUP.sh
source "$HOME/.cargo/env"


cargo install sccache

cd /tmp

wget https://github.com/Kitware/CMake/releases/download/v3.25.1/cmake-3.25.1.tar.gz

tar -xvzf cmake-3.25.1.tar.gz

cd cmake-3.25.1

./bootstrap make

sudo make install


git clone https://github.com/fleek-network/ursa

cd ursa

make install

