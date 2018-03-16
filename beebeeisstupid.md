# local:

ssh into anubis3  
`anubis3`

open a port  
`anubis3_port 8888`

scp things to anubis3  
`scp_to_anubis`

scp things from anubis3
`scp_from_anubis`

# remote:

watch gpu usage  
`watch -n 1 nvidia-smi`

start jupyter notebook  
`CUDA_VISIBLE_DEVICES=0 jupyter notebook . --no-browser`

activate virtualenv  
`source ~/environments/ugly/bin/activate`

check module  
`pip show [package name]`

# open a port and direct to local
on anubis3: `CUDA_VISIBLE_DEVICES=0 jupyter notebook . --no-browser`
on local: `anubis3_port 8888`
open chrome and go to the link

# kill and restart on local
`lsof -n -i:8888 | grep LISTEN`  
`anubis3_port 8888`

4ng31A!
