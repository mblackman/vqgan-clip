# vqgan-clip
Run vqgan + clip locally

Based off: https://colab.research.google.com/drive/15UwYDsnNeldJFHJ9NdgYBYeo6xPmSelP#scrollTo=g7EDme5RYCrt

# Get required packages

git clone https://github.com/openai/CLIP

git clone https://github.com/CompVis/taming-transformers

pip install ftfy regex tqdm omegaconf pytorch-lightning einops transformers ipywidgets torchvision ipython

pip install -e ./taming-transformers

curl -L 'https://heibox.uni-heidelberg.de/d/8088892a516d4e3baf92/files/?p=%2Fconfigs%2Fmodel.yaml&dl=1' > vqgan_imagenet_f16_1024.yaml

curl -L 'https://heibox.uni-heidelberg.de/d/8088892a516d4e3baf92/files/?p=%2Fckpts%2Flast.ckpt&dl=1' > vqgan_imagenet_f16_1024.ckpt

curl -L 'https://heibox.uni-heidelberg.de/d/a7530b09fed84f80a887/files/?p=%2Fconfigs%2Fmodel.yaml&dl=1' > vqgan_imagenet_f16_16384.yaml

curl -L 'https://heibox.uni-heidelberg.de/d/a7530b09fed84f80a887/files/?p=%2Fckpts%2Flast.ckpt&dl=1' > vqgan_imagenet_f16_16384.ckpt

# Notes

If you have a beefy GPU, you will want to process on that. Check if your GPU supports Cuda. To Install CUDA on Windows 10 to get pytorch with Cuda support, run this command:

`pip install torch==1.9.0+cu102 torchvision==0.10.0+cu102 torchaudio===0.9.0 -f https://download.pytorch.org/whl/torch_stable.html`
