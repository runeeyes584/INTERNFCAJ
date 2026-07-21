---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

- Practice IAM Policy restriction rules, configure Switch Role with conditional constraints, and attach IAM Roles to EC2 instances.
- Practice data protection and monitoring: S3 encryption with KMS, logging with CloudTrail, and querying logs using Amazon Athena.
- Learn AWS Database theories including RDS, Aurora, Redshift, and ElastiCache.
- Practice deploying Multi-Tier applications connecting EC2 and RDS within a custom VPC network.

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
      <td style="text-align:center;">11/05/2026</td>
      <td>
        <ul>
          <li> <strong>IAM Permissions Restriction:</strong> Practice creating restriction policies and testing restricted access for IAM Users. </li>
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
      <td style="text-align:center;">12/05/2026</td>
      <td>
        <ul>
          <li> <strong>Security Monitoring:</strong> Configure KMS encryption for S3 bucket, create a trail on CloudTrail, and query activity logs using Amazon Athena. </li>
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
      <td style="text-align:center;">13/05/2026</td>
      <td>
        <ul>
          <li> <strong>Switch Role Configuration:</strong> Configure switch roles with conditional constraints based on source IP and access time. </li>
          <li> <strong>EC2 Credential Security:</strong> Compare using Access Keys versus directly attaching IAM Roles to EC2 when accessing S3. </li>
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
      <td style="text-align:center;">14/05/2026</td>
      <td>
        <ul>
          <li> <strong>AWS Databases:</strong> Study AWS database service theories including RDS, Aurora, Redshift, and ElastiCache. </li>
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
      <td style="text-align:center;">15/05/2026</td>
      <td>
        <ul>
          <li> <strong>RDS Lab Practice:</strong> Build a Multi-Tier VPC network, create subnet groups, launch EC2 app server and RDS instance, test application execution, and test database backup/restore. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/">FCAJ Documentation</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Week 4 Achievements:

- **IAM Access Control & Security**: Practiced setting up permission restriction policies and testing access limitations for IAM Users. Configured Switch Role with conditional constraints based on source IP and time windows. Practiced attaching IAM Roles to EC2 instances instead of manually storing Access Keys.

- **Encryption, Logging & Querying**: Practiced creating KMS keys to encrypt S3 buckets, enabling CloudTrail for activity logging, and using Amazon Athena to query access histories.

- **Databases & Multi-Tier Applications**: Studied overview of AWS database services (RDS, Aurora, Redshift, ElastiCache). Practiced deploying Multi-Tier applications linking EC2 with RDS databases in a custom VPC network and testing database backup/restore features.

- **Learning Progress**: Completed watching and studying videos 187 to 228 in the *First Cloud Journey Bootcamp 2025* series by AWS Study Group.






