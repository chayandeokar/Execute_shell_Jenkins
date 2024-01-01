# Execute_shell_Jenkins

echo "....DevOps CI/CD Started..."
echo "CI/CD Started by user"
whoami

echo "Code Stage"

echo "Build Stage"

systemctl status docker 
docker build -t django-app .

echo "Test Stage"

echo "deploy Stage"

docker run -d -p 8000:8000 django-app:latest

