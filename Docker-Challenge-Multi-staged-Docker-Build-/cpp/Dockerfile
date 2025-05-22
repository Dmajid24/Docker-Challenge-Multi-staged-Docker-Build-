# Stage 1: Build
FROM gcc:latest AS builder

WORKDIR /app
COPY main.cpp .
RUN g++ -o hello main.cpp

# Stage 2: Run (pakai gcc image juga untuk memastikan runtime cocok)
FROM gcc:latest

WORKDIR /app
COPY --from=builder /app/hello .

CMD ["./hello"]
