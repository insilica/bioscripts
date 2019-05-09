# bioscripts
Example works for cancer/bio research

# Running Locally
1. clone this repository
``` 
git clone git@github.com:insilica/bioscripts.git
```

2. Run jupyter/data-science notebook in the clone path
```
docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes \
  -v "$PWD":/home/jovyan/work \
  --name toxtrack-jupyter \ 
  jupyter/datascience-notebook:9b06df75e445
```

3. execute bash on running container
```
docker container exec -it toxtrack-jupyter /bin/bash
```

4. install deepchemenv conda environment
```
conda env create -f ./environment.yml
```

5. add deepchemenv to jupyter kernels
```
python -m ipykernel install --user --name myenv --display-name "deepchemenv"
```
