FROM continuumio/anaconda3

# Force the stdout and stderr streams to be unbuffered.
ENV PYTHONUNBUFFERED 1

# Switch to a non-root user.
RUN useradd -m --uid 1000 dockeruser
ENV HOME /home/dockeruser
USER dockeruser
ENV PATH="/home/dockeruser/.local/bin:${PATH}"

# Working directory
WORKDIR /home/dockeruser/code

# pip install
COPY requirements.txt ./
RUN pip install --user -r requirements.txt

EXPOSE 80

ENTRYPOINT ["jupyter-lab", "--notebook-dir=/home/dockeruser/code/jupyter", "--ip='*'", "--port=80", "--no-browser"]
