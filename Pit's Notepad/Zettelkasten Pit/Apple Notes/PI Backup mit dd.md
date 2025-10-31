<span style="color:#262626ff;"><b>CODE:</b></span> <span style="color:#7601ff;"><b><u>SELECT ALL</u></b></span>
<span style="font-family:Monaco;color:#787878ff;">sudo fdisk -l</span>

<span style="color:#262626ff;">Take note of how the SD card is identified.</span>
<span style="color:#262626ff;">In my case it is /dev/sdb1.</span>
<span style="color:#262626ff;">Then:</span>
<span style="color:#262626ff;"><b>CODE:</b></span> <span style="color:#7601ff;"><b><u>SELECT ALL</u></b></span>
<span style="font-family:Monaco;color:#787878ff;">sudo dd bs=4M if=/dev/sdb | gzip > /home/your_username/image`date +%d%m%y`.gz</span>

<span style="color:#262626ff;">This will compress the image using gzip.</span>
<span style="color:#262626ff;">To restore the backup on SD card:</span>
<span style="color:#262626ff;"><b>CODE:</b></span> <span style="color:#7601ff;"><b><u>SELECT ALL</u></b></span>
<span style="font-family:Monaco;color:#787878ff;">sudo gzip -dc /home/your_username/image.gz | dd bs=4M of=/dev/sdb</span>

<span style="color:#262626ff;">All this must be done on a linux PC.</span>
<span style="color:#262626ff;">It won't work on the raspi!</span>
<span style="color:#000ff;">Posts:</span> <span style="color:#535353ff;">350</span>
<span style="color:#000ff;">Joined:</span> <span style="color:#535353ff;">Tue Jul 24, 2012 10:49 am</span>
<span style="color:#262626ff;">by</span> <span style="color:#757575ff;"><b>erikcf</b></span> <span style="color:#262626ff;">» Wed Jun 12, 2013 9:56 pm</span> 
<span style="color:#262626ff;">In your restore example, I think you need sudo on the dd command rather than gzip, so your example should look like this:</span>

<span style="color:#262626ff;"><b>CODE:</b></span> <span style="color:#7601ff;"><b><u>SELECT ALL</u></b></span>
<span style="font-family:Monaco;color:#787878ff;">gzip -dc /home/your_username/image.gz | sudo dd bs=4M of=/dev/sdb</span>
<span style="color:#000ff;">Posts:</span> <span style="color:#535353ff;">19</span>
<span style="color:#000ff;">Joined:</span> <span style="color:#535353ff;">Thu May 23, 2013 4:17 am</span>
<span style="color:#262626ff;">by</span> <span style="color:#757575ff;"><b>kalehrl</b></span> <span style="color:#262626ff;">» Thu Jun 13, 2013 7:40 am</span> 
<span style="color:#262626ff;"><b>CODE:</b></span> <span style="color:#7601ff;"><b><u>SELECT ALL</u></b></span>
<span style="font-family:Monaco;color:#787878ff;">I think you need sudo on the dd command</span>

<span style="color:#262626ff;">Nope, it works without it.</span>
<span style="color:#262626ff;">There is sudo in front of gzip so I guess it is also applied to the dd command.</span>
<span style="color:#262626ff;">The command lines posted are almost exactly the ones I use myself when backing my SD card.</span>


<span style="color:#262626ff;">ACHTUNG bs=1m (wie Original image große + Mac m klein geschrieben)</span>