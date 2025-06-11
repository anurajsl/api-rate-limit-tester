# API Rate Limiter Testing Tool 🚀

A comprehensive, user-friendly web-based tool for testing API rate limiting behavior. This tool helps developers and system administrators understand how their APIs respond to different traffic patterns and rate limiting scenarios.

![Tool Preview](https://img.shields.io/badge/Status-Ready%20to%20Use-brightgreen)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-blue)
![Browser Compatible](https://img.shields.io/badge/Browser-Compatible-orange)

## 🌟 What This Tool Does

Rate limiting is like having a traffic control system for your API. Just as highways have speed limits to prevent traffic jams, APIs use rate limiting to prevent servers from being overwhelmed by too many requests. This tool helps you test whether these "traffic controls" work correctly under different conditions.

### Key Features

**🎯 Multiple Testing Scenarios**
- **Burst Testing**: Send many requests quickly to simulate sudden traffic spikes
- **Sustained Load Testing**: Maintain steady request rates over extended periods
- **Gradual Increase Testing**: Slowly ramp up request rates to find breaking points
- **Custom Pattern Testing**: Define your own specific testing patterns

**📊 Real-Time Monitoring**
- Live request tracking and success/failure rates
- Response time monitoring and analysis
- Rate limiting detection and reporting
- Interactive charts showing performance trends

**🛠️ Flexible Configuration**
- Support for all HTTP methods (GET, POST, PUT, DELETE)
- Custom headers and request body configuration
- Adjustable timeout and concurrency settings
- Easy API endpoint switching

**📈 Detailed Analytics**
- Comprehensive logging of all requests and responses
- Statistical analysis of response times
- Rate limiting pattern identification
- Export-ready test results

## 🚀 Quick Start

### Option 1: Direct Use (Recommended for beginners)
1. Download the `rate-limiter-tester.html` file
2. Double-click it to open in your web browser
3. Enter your API endpoint URL
4. Click "Start Test" and watch the magic happen!

### Option 2: Web Server (For advanced users)
If you want to serve it from a web server, simply place the HTML file in your web directory.

## 💡 How To Use

### Basic Setup
1. **Enter Your API Details**: Put your API endpoint URL in the first field
2. **Choose HTTP Method**: Select GET, POST, PUT, or DELETE based on your API
3. **Add Headers**: Include any authentication tokens or special headers your API needs
4. **Select Test Scenario**: Pick from burst, sustained, gradual, or custom testing

### Understanding Test Scenarios

**🚀 Burst Test**
Perfect for testing how your API handles sudden traffic spikes, like when a social media post goes viral. This sends many requests very quickly to see if your rate limiter can handle the surge.

**⏱️ Sustained Load**
Tests how your API performs under steady, continuous traffic. Think of this like testing how well your car performs during a long highway drive at constant speed.

**📈 Gradual Increase**
Slowly increases the request rate to find exactly where your rate limiter starts working. This is like gradually pressing the accelerator to find your car's top speed.

**⚙️ Custom Pattern**
Lets you define your own testing pattern for specific scenarios unique to your application.

### Reading the Results

The tool provides several types of feedback:

**Status Cards**: Show real-time counts of successful requests, rate-limited requests, and errors
**Progress Bar**: Visual indicator of test completion
**Live Log**: Detailed information about each request and response
**Charts**: Visual representation of response times and request patterns over time

## 🔧 Configuration Options

### Request Settings
- **Requests per Second**: How many requests to send each second (1-100)
- **Test Duration**: How long to run the test in seconds (1-300)
- **Max Concurrent**: Maximum simultaneous requests (1-100)
- **Timeout**: How long to wait for responses in milliseconds (1000-30000)

### API Configuration
- **Endpoint URL**: Your API's full URL
- **HTTP Method**: The type of request to make
- **Headers**: Authentication and other required headers in JSON format
- **Request Body**: Data to send with POST/PUT requests

## 📋 Example Use Cases

### Testing E-commerce API
```
Scenario: Black Friday traffic simulation
- Use Burst Test with 50 RPS for 30 seconds
- Monitor for 429 (Too Many Requests) responses
- Check if legitimate users can still make purchases
```

### Testing Authentication Service
```
Scenario: Login attempt rate limiting
- Use Sustained Load with 10 RPS for 60 seconds
- Include authentication headers
- Verify rate limiting kicks in after expected threshold
```

### Testing Public API
```
Scenario: Finding optimal rate limits
- Use Gradual Increase from 1-20 RPS over 120 seconds
- Monitor when rate limiting begins
- Adjust your API's rate limits based on results
```

## 🛡️ Important Notes

### Responsible Testing
- **Only test APIs you own or have permission to test**
- **Start with low request rates** to avoid overwhelming servers
- **Be mindful of costs** if testing cloud-based APIs that charge per request
- **Respect rate limits** - this tool is for testing, not for bypassing limits

### Best Practices
- Test during off-peak hours when possible
- Monitor your server resources during testing
- Keep test durations reasonable to avoid unnecessary load
- Document your findings for future reference

### Troubleshooting
- **CORS Errors**: Some APIs block browser requests. Use a CORS proxy or test APIs designed for browser access
- **Network Errors**: Check your internet connection and API endpoint URL
- **Timeout Issues**: Increase timeout values for slow APIs
- **High Error Rates**: Reduce request rate or check API authentication

## 🤝 Contributing

Found a bug or have a feature idea? Here's how you can help:

1. **Report Issues**: Describe what happened and what you expected
2. **Suggest Features**: Tell us what would make this tool more useful
3. **Share Examples**: Show us interesting rate limiting patterns you've discovered
4. **Improve Documentation**: Help make these instructions even clearer

## 📝 Technical Details

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### No External Dependencies
This tool runs entirely in your browser with no external libraries or dependencies. Everything you need is contained in the single HTML file.

### Privacy and Security
- All testing happens directly between your browser and the target API
- No data is sent to external servers
- All configuration and results stay on your local machine

## 📚 Learning Resources

### Understanding Rate Limiting
Rate limiting is a crucial aspect of API design that prevents abuse and ensures fair usage. If you're new to this concept, think of it like a bouncer at a popular restaurant who controls how many people can enter at once.

### HTTP Status Codes
- **200 OK**: Request successful
- **429 Too Many Requests**: Rate limit exceeded
- **500 Internal Server Error**: Server problem
- **503 Service Unavailable**: Server overloaded

### Performance Metrics
- **Response Time**: How long each request takes
- **Throughput**: How many requests completed per second
- **Error Rate**: Percentage of failed requests
- **Success Rate**: Percentage of successful requests

## 🏷️ Version History

### v1.0.0 - Initial Release
- Complete rate limiter testing functionality
- Multiple testing scenarios
- Real-time monitoring and charts
- Comprehensive logging system
- User-friendly interface

## 📞 Support

If you need help using this tool:
1. Check the troubleshooting section above
2. Review the example use cases
3. Look at the configuration options carefully
4. Try starting with simple tests before complex ones

Remember, testing rate limiters is both an art and a science. Start simple, observe the results, and gradually increase complexity as you learn how your API behaves.

---

**Happy Testing!** 🎉

*This tool was created to help developers build better, more resilient APIs. Use it wisely and responsibly.*
