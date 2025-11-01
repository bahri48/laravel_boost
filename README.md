## Install Laravel
laravel new ProjectName

## install Laravel Boost
https://boost.laravel.com/installed 
1. migrate your database "php artisan migrate"
2. composer require laravel/boost --dev
3. php artisan boost:install
    -vscode
    -claude_code

    
## Check Commad Boost
php artisan

 boost
  boost:install   => Install Laravel Boost
  boost:mcp       => Starts Laravel Boost (usually from mcp.json)
  boost:update    => Update the Laravel Boost guidelines to the latest guidance

## Setup Using Code Editors
VS Code
1. Open the Command Palette (Cmd+Shift+P or Ctrl+Shift+P)
2. Press enter on "MCP: List Servers"
3. Arrow to laravel-boost and press 'enter'
4. Choose 'Start server' and you're good to go!


## Setup Using Claude CLI
1. claude mcp add laravel-boost --scope project -- php artisan boost:mcp
2. claude mcp add sequential-thinking --scope project -- npx -y @modelcontextprotocol/server-sequential-thinking
3. claude mcp add herd --scope project --env SITE_PATH="D:\DirektoryName\DirektoryProject" -- php C:/Users/<UserComputerName>/.config/herd/bin/herd-mcp.phar
perintah diatas akan menghasilkan file .mcp.json dan kode berikut ini:
{
  "mcpServers": {
    "laravel-boost": {
      "type": "stdio",
      "command": "php",
      "args": [
        "artisan",
        "boost:mcp"
      ],
      "env": {}
    },
    "sequential-thinking": {
      "type": "stdio",
      "command": "cmd", // rubah npx menjadi cmd
      "args": [
        "/c", // tambahkan baris ini
        "npx", // tambahkan baris ini
        "-y",
        "@modelcontextprotocol/server-sequential-thinking"
      ],
      "env": {}
    },
    "herd": {
      "type": "stdio",
      "command": "php",
      "args": [
        "C:/Users/LabKom/.config/herd/bin/herd-mcp.phar"
      ],
      "env": {
        "SITE_PATH": "D:\\Koding\\laravel_boost"
      }
    }
  }
}
