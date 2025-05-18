<h1 align="left">GoMFT - Go Managed File Transfer</h1>

GoMFT is a web-based managed file transfer application built with Go, leveraging rclone for robust file transfer capabilities. It provides a user-friendly interface for configuring, scheduling, and monitoring file transfers across various storage providers.

---


## Features

- **Multiple Storage Support**: Leverage rclone's extensive support for cloud storage providers:
  - Google Drive
  - Google Photos
  - Amazon S3
  - MinIO
  - NextCloud
  - WebDAV
  - SFTP
  - FTP
  - SMB/CIFS shares
  - Hetzner Storage Box
  - Backblaze B2
  - Wasabi
  - Local filesystem
  - And more via rclone
- **Webhook Notifications**: Receive real-time notifications of job events:
  - Configurable webhook URLs
  - HMAC-SHA256 authentication with secrets
  - Custom HTTP headers
  - Selectable events (job success, job failure)
  - Detailed JSON payload with job information
- **Multiple Notification Services**: Get job status updates through various notification channels:
  - Email notifications with configurable SMTP settings
  - Webhooks with authentication for custom integrations
  - Pushbullet notifications with optional device targeting
  - Ntfy.sh (both public and self-hosted) for simple push notifications
  - Gotify server integration for self-hosted notifications
  - Pushover notifications with customizable sounds and priorities
  - Configurable message templates for all notification types
  - Event-based triggers (job start, completion, errors)
- **Scheduled Transfers**: Configure transfers using cron expressions with flexible scheduling options
- **Transfer Monitoring**: Real-time status updates and detailed transfer logs with bytes and files transferred statistics
- **File Metadata Tracking**: Complete history and status of all transferred files with detailed information:
  - Process status (processed, archived, deleted)
  - File size and hash information
  - Advanced search and filtering capabilities
  - Metadata retention for compliance and auditing
  - Detailed file view with processing timestamps and job association
  - Powerful filtering by status, filename, job, and date ranges
  - Advanced search interface with multiple criteria
  - Bulk management and record deletion capabilities
  - Responsive design with mobile-friendly interface
- **Multi-threaded File Transfers**: Significantly improve performance with concurrent file processing:
  - Configurable number of concurrent transfers (1-32) per job
  - Automatic queue management to prevent system overload
  - Independent configuration for each transfer job
  - Optimized for both high-volume small files and large file transfers
  - Maximizes bandwidth utilization for cloud storage providers
- **Web Interface**: User-friendly interface for managing transfers, built with Templ components
- **File Pattern Matching**: Support for file patterns to filter files during transfers
- **File Output Patterns**: Dynamic naming of destination files using patterns with date variables
- **Archive Function**: Option to archive transferred files for backup and compliance
- **Transfer Configurations**: Full control over source and destination connection parameters
- **Job Management**: Create, edit, and monitor transfer jobs with scheduling
- **Security**: Role-based access control with admin-managed user accounts and secure password management
- **Authentication Providers**: Flexible authentication options:
  - Built-in email/password authentication
  - Authentik integration for enterprise SSO
  - OpenID Connect (OIDC) support for standard identity providers
  - OAuth2 integration for popular providers (Google, GitHub, etc.)
  - Multiple provider support with fallback options
  - Automatic user provisioning from external providers
  - Role mapping from external identity providers
- **Password Recovery**: Self-service password reset via email with secure token-based authentication
- **User Profile Management**: Personal settings including theme preferences
- **Modern UI**: Built with Templ, HTMX and Tailwind CSS for a responsive experience
- **Docker Support**: Easy deployment with Docker images and Docker Compose support
- **Portable Deployment**: Run on any platform that supports Docker or Go