# Docker Files

A collection of custom Docker containers for building and testing R packages

## Docker images currently available
<pre>
rocker/r-ver (Docker image)
 │
hadley/devtools (R package)
 │
<b>ruaridhw/r-pkgdev</b> (Docker image)
 │
 ├── leeper/rio (R package) ─── <b>ruaridhw/rio</b> (Docker image)
 │
mono:3.12.1 (Docker image)
 │
 └── jmp75/rClr (R package) ─── <b>ruaridhw/rclr</b> (Docker image)
         │
    microsoft/mssql-server-linux (Docker image)
         │
         └── agstudy/rsqlserver (R package) ─── <b>ruaridhw/rsqlserver</b> (Docker image)
                                                           │
                                                           └── rocker/rstudio (Docker image) ─── <b>ruaridhw/rsqlserver-rstudio</b> (Docker image)
</pre>
