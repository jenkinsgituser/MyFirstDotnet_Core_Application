"# MyFirstDotnet_Core_Application" 


…or create a new repository on the command line
echo "# MyFirstDotnet_Core_Application" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/jenkinsgituser/MyFirstDotnet_Core_Application.git
git push -u origin master
                
…or push an existing repository from the command line
git remote add origin https://github.com/jenkinsgituser/MyFirstDotnet_Core_Application.git
git push -u origin master

================================#############################================================

mkdir PrimeService
mkdir PrimeService.Tests
dotnet new mvc -o PrimeService
dotnet new nunit -o PrimeService.Tests
dotnet new sln -n PrimeService
dotnet sln add PrimeService/PrimeService.csproj

dotnet restore PrimeService.sln
dotnet restore PrimeService/PrimeService.csproj

dotnet build PrimeService.sln
dotnet build PrimeService/PrimeService.csproj

dotnet sln PrimeService.sln add PrimeService.Tests/PrimeService.Tests.csproj

dotnet restore PrimeService.sln
dotnet restore PrimeService.Tests/PrimeService.Tests.csproj

dotnet build PrimeService.sln
dotnet build PrimeService.Tests/PrimeService.Tests.csproj

dotnet test PrimeService.sln
dotnet test PrimeService/PrimeService.csproj

dotnet add PrimeService.Tests/PrimeService.Tests.csproj reference PrimeService/PrimeService.csproj

dotnet add PrimeService package moq

================================#############################================================