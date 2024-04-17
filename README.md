# NSC
ssh -L 8895:localhost:8895 -o "ProxyCommand=nc -X 5 -x proxy-us.intel.com:1080 %h %p" -tt webinar@IP					

 

docker run -itd --name test --runtime=habana -e HABANA_VISIBLE_DEVICES=all -e OMPI_MCA_btl_vader_single_copy_mechanism=none --cap-add=sys_nice --net=host --ipc=host  -v /var/run/docker.sock:/var/run/docker.sock vault.habana.ai/gaudi-docker/1.14.0/ubuntu22.04/habanalabs/pytorch-installer-2.1.1:latest



docker exec -it test bash

cd ~

git clone https://github.com/habanaai/Gaudi2-Workshop

git clone https://www.github.com/habanaai/Gaudi-tutorials



python3 -m pip install jupyterlab && python3 -m jupyterlab_server --ServerApp.ip='*' --IdentityProvider.token='' --ServerApp.password='' --allow-root --port 8895 --ServerApp.root_dir=/root &

http://<IP>:8895/lab

Now you can run the three Gaudi Workshop tutorials:

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/PyTorch-Inference/stable_diffusion_v_2_1.ipynb

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/Model-Migration/model_migrate.ipynb

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/LLM-Training/Hugging%20Face%20Large%20Language%20Model%20Habana.ipynb


 

Now you can run the three Gaudi Workshop tutorials:

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/PyTorch-Inference/stable_diffusion_v_2_1.ipynb

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/Model-Migration/model_migrate.ipynb

https://github.com/HabanaAI/Gaudi2-Workshop/blob/main/LLM-Training/Hugging%20Face%20Large%20Language%20Model%20Habana.ipynb
