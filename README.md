# b
Setting up config on MacOS Catalina. Influenced by Burke Libbey, Luc Perkins.

## Usage

1. [Install Nix](https://nixos.org/manual/nix/stable/#sect-macos-installation)

    ```console
    sh <(curl -L https://nixos.org/nix/install) --darwin-use-unencrypted-nix-store-volume
    ```

2. Add the [Home Manager](https://github.com/nix-community/home-manager/blob/master/README.md) channel

    ```console
    $ nix-channel --add https://github.com/nix-community/home-manager/archive/master.tar.gz home-manager
    $ nix-channel --update
    ```

3. Install Home Manager and create the first Home Manager generation:

    ```console
    $ nix-shell '<home-manager>' -A install
    ```

4. Clone [repo](https://github.com/cchalc/b)

    ```console
    $ git clone https://github.com/cchalc/b.git nixpkgs
    ```

5. Run home-manager switch

    ```console
    $ home-manager switch && source ~/.zshrc
    ```
