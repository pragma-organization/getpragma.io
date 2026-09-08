# getpragma.io

Static one-page website for `getpragma.io`. It has no framework, build step, external scripts, fonts, images, or trackers.

## GitHub Pages

1. Create the repository `pragma-organization/getpragma.io`.
2. Push `main`.
3. Open `Settings -> Pages`.
4. Choose `Deploy from a branch`, then select `main` and `/ (root)`.
5. Set the custom domain to `getpragma.io`.
6. Select `Enforce HTTPS` after the DNS check passes.

At the registrar, add A records for the apex to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`. Add a CNAME for `www` to `pragma-organization.github.io`. Expect up to an hour for DNS.

## S3 + CloudFront alternative

1. Upload the static files to an S3 bucket configured as the CloudFront origin.
2. Create a CloudFront distribution with an ACM certificate for `getpragma.io` and `www.getpragma.io`.
3. Point the apex and `www` DNS records to the CloudFront distribution.
