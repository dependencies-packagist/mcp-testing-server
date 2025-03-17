# Model Context Protocol (SDK) Testing Servers

This is a web-based application for testing MCP servers. It was designed to demonstrate a MCP client capable of running in a typical web hosting environment.

### Using The Web Client

To connect to the included MCP test server, enter `php` in the Command field and `server.php` in the Arguments field and click `Connect to Server`. The interface allows you to test Prompts, Tools, and Resources. There is also a Debug Panel allowing you to view the JSON-RPC messages being sent between the Client and Server.

### Web Client Notes And Limitations

This MCP Web Client is intended for developers to test MCP servers, and it is not recommended to be made publicly accessible as a web interface without additional testing for security, error handling, and resource management.

While MCP is usually implemented as a stateful session protocol, a typical PHP-based web hosting environment restricts long-running processes. To maximize compatibility, the MCP Web Client will initialize a new connection between the client and server for every request, and then close that connection after the request is complete.

## Installation

You can install the package via [Composer](https://getcomposer.org/):

```bash
composer create-project mcp/testing-server mcp-client
```

```bash
php server.php
```

```bash
php -S 127.0.0.1:8989
```

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.
