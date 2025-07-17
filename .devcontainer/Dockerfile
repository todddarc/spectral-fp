# ---------- base image with micromamba ----------
FROM mambaorg/micromamba:1.5.2-bullseye

# ---------- install everything from conda‑for­ge ----------
RUN micromamba install -y -n base -c conda-forge \
    python=3.11            \
    shenfun               \
    mpich mpi4py mpi4py-fft \
    numpy scipy            \
 && micromamba clean -afy

# ---------- optional: Jupyter kernel --------------
RUN python -m ipykernel install --prefix /usr/local \
    --name shenfun --display-name "Python (shenfun)"
