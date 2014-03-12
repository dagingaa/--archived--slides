![](http://i.imgur.com/dG4sZwO.png)
note:
    - We run everything with NodeJS, Express for HTTP stuff and SokcetIO for WebSockets
    - The server is entierly (well, almost) stateless
    - All state is kept in SimpleDB, allows us to scale if we have to
    - Recently launched reconnecting to room meaning no downtime visible for users
    - Only one node, hosted on Amazon EC2
    - Static assets are uplaoded to S3 and pushed through CloudFront. Use Grunt to do CDNifying of assets
    - Frontend is built around AngularJS
    - Everything else is completely custom written
    - We use all the new cool web technology
    - Flexbox, filters, transitions, animations, soon maybe web components
    - Demands a lot form the team, keeping up with new development
    - Try to integrate learning with actual development, experimental features
      need to be experimented with
    - If we find a browser bug (we've found a few), we report and wait 6-8 weeks before implementing it
