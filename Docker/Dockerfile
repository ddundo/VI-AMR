# Dockerfile for installing Firedrake with ALL mesh adaptation support via Mmg,
# ParMmg, Netgen, Animate, Movement, and Goalie

# Use a base image with Firedrake and mesh adaptation dependencies pre-installed
FROM ghcr.io/mesh-adaptation/firedrake-parmmg:latest

USER firedrake
WORKDIR /home/firedrake

# Install VI-AMR and its dependencies
# Netgen is installed via ngsPETSc
RUN pip install ngsPETSc shapely siphash24 pandas matplotlib && \
    git clone https://github.com/StefanoFochesatto/VI-AMR.git && \
    pip install -e VI-AMR
