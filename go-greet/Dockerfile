# Menggunakan basis image golang terbaru
FROM golang:latest

# Mengatur Working Directory di dalam container
WORKDIR /app

# Menyalin file go.mod dan go.sum
COPY go.mod ./

# Mendownload semua modul go yang menjadi dependensi
RUN go mod download

# Menyalin sourcecode dari direktori aktif ke Working Directory di dalam container
COPY . .

# Build aplikasi web berbasis go
RUN go build -o main .

# Expose port 8080
EXPOSE 8080

# Menjalankan aplikasi web
CMD ["./main"]