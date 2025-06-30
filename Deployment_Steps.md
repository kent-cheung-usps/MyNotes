## Deployment Steps

`Thanks to Partick Wilkerson for providing the information.`

#### 1. Checkout the Branch You Want to Tag
   `git checkout your-branch-name`

#### 2. Create a Tag
   `git tag release-dev3-[tag_name]`
   OR
   `git tag -a release-dev3-[tag_name] -m "Message Note"`

#### 3. Push the Tag
   `git push origin release-dev3-[tag_name]`

To build under Jenkins for DEV environments use the format:
- DEV1 : release-dev-[your tag name]
- DEV2 : release-dev2-[your tag name]
- DEV3 : release-dev3-[your tag name]

This will setup DEV3 for `release-dev3-My-Code`
 
#### 4. Deploy to Dev Env
- Next you you login into Jenkins (https://ebs.usps.gov/job/app/job/9075/)
- Go to "COP Multibranch Pipeline" and select "Tags" to see your tag
- Select the Play button to begin building your tag. And from there you can click on your tag to see the progress of your build.

