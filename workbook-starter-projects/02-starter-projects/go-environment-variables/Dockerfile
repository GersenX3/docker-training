# Etapa de compilación
FROM golang:tip-alpine3.22
WORKDIR /app
COPY . .
# RUN go build -o main .

# # Etapa de ejecución
# FROM scratch
# WORKDIR /
# COPY --from=builder /app/main .
CMD ["go", "run", "main.go"]