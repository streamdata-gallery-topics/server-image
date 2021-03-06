---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Describe Images
  version: 1.0.0
  description: Describes one or more of the images (AMIs, AKIs, and ARIs) available
    to you.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CopyImage:
    get:
      summary: Copy Image
      description: Initiates the copy of an AMI from the specified source region to
        the current region.
      operationId: copyimage
      x-api-path-slug: actioncopyimage-get
      parameters:
      - in: query
        name: BlockDeviceMapping.N
        description: Information about one or more block device mappings
        type: string
      - in: query
        name: Description
        description: A description for the new image
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: Name
        description: A name for the new image
        type: string
      - in: query
        name: NoReboot
        description: By default, Amazon EC2 attempts to shut down and reboot the instance
          before creating the image
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Image
  /?Action=CreateImage:
    get:
      summary: Create Image
      description: Creates an Amazon EBS-backed AMI from an Amazon EBS-backed instance
        that is either running or stopped.
      operationId: createimage
      x-api-path-slug: actioncreateimage-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: ImageId
        description: The ID of the AMI
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Image
  /?Action=DeregisterImage:
    get:
      summary: Deregister Image
      description: Deregisters the specified AMI.
      operationId: deregisterimage
      x-api-path-slug: actionderegisterimage-get
      parameters:
      - in: query
        name: Attribute
        description: The AMI attribute
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: ImageId
        description: The ID of the AMI
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Image
  /?Action=DescribeImageAttribute:
    get:
      summary: Describe Image Attribute
      description: Describes the specified attribute of the specified AMI.
      operationId: describeimageattribute
      x-api-path-slug: actiondescribeimageattribute-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: ExecutableBy.N
        description: Scopes the images by users with explicit launch permissions
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: ImageId.N
        description: One or more image IDs
        type: string
      - in: query
        name: Owner.N
        description: Filters the images by the owner
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Image
  /?Action=DescribeImages:
    get:
      summary: Describe Images
      description: Describes one or more of the images (AMIs, AKIs, and ARIs) available
        to you.
      operationId: describeimages
      x-api-path-slug: actiondescribeimages-get
      parameters:
      - in: query
        name: Attribute
        description: The name of the attribute to modify
        type: string
      - in: query
        name: Description
        description: A description for the AMI
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: ImageId
        description: The ID of the AMI
        type: string
      - in: query
        name: LaunchPermission
        description: A launch permission modification
        type: string
      - in: query
        name: OperationType
        description: The operation type
        type: string
      - in: query
        name: ProductCode.N
        description: One or more product codes
        type: string
      - in: query
        name: UserGroup.N
        description: One or more user groups
        type: string
      - in: query
        name: UserId.N
        description: One or more AWS account IDs
        type: string
      - in: query
        name: Value
        description: The value of the attribute being modified
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Image
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---