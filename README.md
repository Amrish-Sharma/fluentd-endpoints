# Fluentd Docker Image with Multiple Plugins

This repository contains a Dockerfile and accompanying resources for building a Fluentd Docker image with various plugins enabled, including S3, HTTP, Splunk, and Elastic, allowing users to send events to multiple outputs.

## Usage

### Building the Image

To build the Docker image, run the following command in the root directory of this repository:

```bash
docker build -t fluentd-with-plugins .
```

### Running the Container

Once the image is built, you can run the container with the desired configurations. Make sure to mount your Fluentd configuration file into the container at `/fluentd/etc/fluent.conf` and any additional configuration files or plugins in `/fluentd/etc/`.

```bash
docker run -v /path/to/your/fluent.conf:/fluentd/etc/fluent.conf -v /path/to/your/additional/config:/fluentd/etc/ -d fluentd-with-plugins
```

### Configuration

Configure Fluentd according to your requirements by modifying the `fluent.conf` file. You can include configurations for various plugins like S3, HTTP, Splunk, and Elastic to define the desired outputs.

### Plugins

This Docker image includes the following plugins:

- **S3**: Allows sending logs to Amazon S3 buckets.
- **HTTP**: Enables sending logs over HTTP.
- **Splunk**: Supports sending logs to Splunk servers.
- **Elastic**: Facilitates sending logs to Elasticsearch.

## Contributing

If you have any suggestions, improvements, or additional plugins to add, feel free to open an issue or create a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
