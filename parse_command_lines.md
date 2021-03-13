> Bash script  to parse command line arguments. The following notes are from [parsing command line arguments in Bash](https://dev.to/unfor19/parsing-command-line-arguments-in-bash-3b51).
## The usual way

Save variables in four different places. 

1 - usage function

The  `usage`  function should pop up whenever the user attempts to provide wrong or missing arguments
```
usage()
{
cat << EOF
usage: bash ./scripts/packndeploy -n service_name
-n    | --service_name      (Required)            Service to deploy
-b    | --branch            (master)              Source branch
-h    | --help                                    Brings up this menu
EOF
}
```
### 2 - Declaring Variables

To get the command line arguments, we need to declare variables that can store them, and also set the default values for these variables/arguments.
```
service_name=
branch=master # default value
```
### 3 - Arguments to Variables

Mapping arguments to variables with  `while case shift`  is a great trick to fetch variables! To learn more about it read this  [great tutorial](http://linuxcommand.org/lc3_wss0120.php)  or this great comment in  [StackOverflow](https://stackoverflow.com/a/14203146/5285732)
```
while [ "$1" != "" ]; do
    case $1 in
        -n | --service_name )
            shift
            service_name=$1
        ;;
        -b | --branch )
            shift
            branch=$1              
        -h | --help )    usage
            exit
        ;;
        * )              usage
            exit 1
    esac
    shift
done
```
### 4 - Verifying required arguments

After the  `while`  loop above, we need to make sure that the required variables were provided. So here's a quick and dirty way to do it.
```
if [ -z $service_name ]; then
    echo "Service name is required, provide it with the flag: -n service_name"
    exit
fi
```

