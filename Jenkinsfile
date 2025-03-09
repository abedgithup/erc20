import subprocess

def run_command(command):
    """Run a shell command and handle errors."""
    print(f'Running command: {command}')
    try:
        subprocess.run(command, check=True, shell=True)
    except subprocess.CalledProcessError as e:
        print(f'Error occurred: {e}')
        exit(1)

def clone_repository():
    run_command('git clone https://github.com/your-repo.git')

def build():
    run_command('mvn clean install')  # Modify for Maven: run_command('mvn clean package')

def test():
    run_command('mvn test')

def deploy():
    run_command('docker build -t my-app .')
    run_command('docker run -d -p 8080:8080 my-app')

if __name__ == '__main__':
    clone_repository()
    build()
    test()
    deploy()
