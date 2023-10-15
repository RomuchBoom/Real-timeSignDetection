FROM python:3.8

WORKDIR D:\ML\envs\SignDetection\Filter\Build

COPY DnD_Real-time_Sign_Recognition.ipynb requirements.txt ./

RUN pip install --upgrade pip

RUN apt-get update && apt-get install ffmpeg libsm6 libxext6  -y

RUN pip install -r requirements.txt

EXPOSE 8888

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]