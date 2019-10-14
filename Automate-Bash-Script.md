## Code Format:

`filename.sh locale fromgiturl fromgitbranch togiturl togitbranch`

### For Windows

`bash ./build.sh en-NZ git@gitlab.com:project-eva/nz-site.git dev git@gitlab.com:project-eva/us-region.git zespriqa`

### For Linux

`sh ./build.sh en-NZ git@gitlab.com:project-eva/nz-site.git dev git@gitlab.com:project-eva/us-region.git zespriqa`



Use the below attached `build.sh` file for automate the build and deployment
-   

If we don't want to copy the build in our local computer folder. Just comment the line 43. 
Or If we want to copy the folder just update your correct local folder path eg `../AMainRepo/build` in my case. 


### CODES:

- `bash ./build.sh en-US git@gitlab.com:project-eva/usa-site.git dev git@gitlab.com:project-eva/us-region.git zespriqa`

- `bash ./build.sh ko-KR git@gitlab.com:project-eva/korea-site.git dev git@gitlab.com:project-eva/us-region.git zespriqa`

- `bash ./build.sh en-NZ git@gitlab.com:project-eva/nz-site.git dev git@gitlab.com:project-eva/us-region.git zespriqa`







