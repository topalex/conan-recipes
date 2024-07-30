# Conan local recipes
For packages not available in conan center

### Currently available packages
- librsvg (requires `rustc`, `cargo`, `cargo-c` to build)

## Usage
Clone repo:
```
git clone https://github.com/topalex/conan-recipes.git
```
Add as local remote:
```
conan remote add mylocalrepo ./conan-recipes --allowed-packages=\"librsvg/*\"
```
Now you can use repo to install packages:
```
conan list "*" -r=mylocalrepo
conan install --requires=librsvg/2.58.92 --build=missing
```
