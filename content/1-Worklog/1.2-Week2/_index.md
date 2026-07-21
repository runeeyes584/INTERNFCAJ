---
title: "Week 2 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

- Complete AWS Transit Gateway labs to wrap up Module 02 on Networking.
- Gain deep knowledge of Amazon EC2 (Instance Types, AMIs, EBS, Instance Store, User Data, Metadata, and Auto Scaling).
- Practice AWS Backup for EC2 and master the backup/restore workflow.
- Research and practice deploying AWS Storage Gateway and configuring File Share.
- Master Amazon S3 features (Static Website Hosting, CloudFront integration, Bucket Versioning, and Cross-Region Replication).
- Understand the overview of AWS Storage services and begin migrating Virtual Machines from On-premises to AWS.

### Tasks to be carried out this week:

<table> 
  <thead>
    <tr>
      <th style="text-align:center;">Day</th>
      <th style="text-align:center;">Date</th>
      <th style="text-align:center;">Task</th>
      <th style="text-align:center;">Reference Material</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">2</td>
      <td style="text-align:center;">27/04/2026</td>
      <td>
        <ul>
          <li> <strong>Basic EC2:</strong> Learn about Instance Types, AMIs, and Key Pairs. </li>
          <li> <strong>Advanced EC2 (Part 1):</strong> Hands-on with Elastic Block Store (EBS), Instance Store, User Data (bootstrap scripts), and EC2 Metadata Service. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">28/04/2026</td>
      <td>
        <ul>
          <li> <strong>Advanced EC2 (Part 2):</strong> Hands-on with EC2 Auto Scaling, EFS, FSx, Lightsail, and MGN. </li>
          <li> <strong>Transit Gateway:</strong> Create Transit Gateway, Attachments, Route Tables, and update VPC Route Tables. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">29/04/2026</td>
      <td>
        <ul>
          <li> <strong>Storage Gateway (Full package):</strong> Create S3 Bucket, launch EC2 for Storage Gateway, configure Storage Gateway and File Share. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">30/04/2026</td>
      <td>
        <ul>
          <li> <strong>AWS Backup:</strong> Deploy Backup infrastructure, create Backup Plans, test Restore from Recovery Points, configure Backup notifications. </li>
          <li> <strong>S3 Static Website Hosting:</strong> Create bucket, configure Public Access and Bucket Policy, set up CloudFront distribution and test content delivery. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">01/05/2026</td>
      <td>
        <ul>
          <li> <strong>Advanced S3:</strong> Hands-on with Bucket Versioning, Object Lifecycle, and Cross-Region Replication. </li>
          <li> <strong>Theory Review:</strong> Module 04 Storage Overview (Advanced S3, Snow Family, Storage Gateway, Backup). </li>
          <li> <strong>Migration:</strong> Start VM migration process (VMware Workstation, Export VM, Upload & Import to AWS). </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/vi/2-migrate/">FCAJ Documentation</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Week 2 Achievements:

- **Networking & EC2 Infrastructure**: Completed AWS Transit Gateway setup (multi-VPC Attachments, inter-VPC Route Tables). Learned key EC2 concepts (Instance Types, AMIs, Key Pairs, EBS, Instance Store, User Data, Metadata, Auto Scaling) and related services (EFS, FSx, Lightsail, AWS MGN).

- **Storage, Backup & Storage Gateway**: Explored the AWS Storage ecosystem (S3, Glacier, Snow Family, Storage Gateway, AWS Backup). Successfully practiced deploying AWS Backup infrastructure (Backup Plans, Recovery Points, EC2 restore) and configuring AWS Storage Gateway File Share with Amazon S3.

- **Amazon S3 & CloudFront Content Delivery**: Studied S3 data management mechanisms (Bucket Policy, Public Access control, Storage Classes, Access Points, Versioning, Lifecycle, CRR). Practiced deploying S3 Static Website Hosting integrated with CloudFront Distribution.

- **VM Migration & Troubleshooting**: Practiced the VM migration process from On-premises to AWS (exporting VM from VMware Workstation, uploading to S3, importing AMI, and launching EC2). Learned to resolve common practical issues (Transit Gateway Attachments, EBS, Bucket Policies, CloudFront origins, S3 Replication, VM Import).

- **Learning Progress**: Completed watching and studying videos 65 to 120 in the *First Cloud Journey Bootcamp 2025* series by AWS Study Group.






