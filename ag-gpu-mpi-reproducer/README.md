1. Get an interactive session with 2 GPUs (e.g. salloc --nodes=1 --gpus-per-node=2 --tasks-per-node=2 --time=00:30:00).
2. Source the relevant environment file.
3. cmake -S . -B build && cmake --build build && srun -n 2 ./build/gpu_pingpong.
4. If GPU-aware MPI is not supported, this will crash. Running gpu_pingpong with --stage-via-host should work.
