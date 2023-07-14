
## GDB

### PwnDBG

```sh
git clone https://github.com/pwndbg/pwndbg
cd pwndbg
./setup.sh
cd ..
mv pwndbg ~/pwndbg-src
echo "source ~/pwndbg-src/gdbinit.py" > ~/.gdbinit_pwndbg
```

[Official Github](https://github.com/pwndbg/pwndbg)

### PEDA

```sh
git clone https://github.com/longld/peda.git ~/peda
```

[Official Github](https://github.com/longld/peda)

### GEF

```sh
wget -q -O ~/.gdbinit-gef.py https://github.com/hugsy/gef/raw/master/gef.py
echo source ~/.gdbinit-gef.py >> ~/.gdbinit
```

[Official Github](https://github.com/hugsy/gef)

### Final steps

After all the above have been done you have to open the `~/.gdbinit` file and paste the following in

```sh
define init-peda
source ~/peda/peda.py
end
document init-peda
Initializes the PEDA (Python Exploit Development Assistant for GDB) framework
end

define init-pwndbg
source ~/.gdbinit_pwndbg
end
document init-pwndbg
Initializes PwnDBG
end

define init-gef
source ~/.gdbinit-gef.py
end
document init-gef
Initializes GEF (GDB Enhanced Features)
end
```

## Ropper

```sh
pip install capstone
pip install filebytes
pip install keystone-engine
pip install ropper
```

[Official Github](https://github.com/sashs/Ropper)

### Checksec

```sh
apt install checksec
```

[Official Github](https://github.com/slimm609/checksec.sh)