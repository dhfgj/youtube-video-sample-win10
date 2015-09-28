# Youtube Video Sample - Windows 10
This sample will show you how to get a Youtube Channel/Playlist Videos and set it as a player source on your Windows 10 App.
It's based on the <a target="_blank" href="https://developers.google.com/youtube/">Youtube Data API.</a>

P.S : This sample is updated to use Youtube Data API v3

<h2>Building the Sample</h2>
Before starting this sample, you need to know <a target="_blank" href="http://docs.nuget.org/docs/start-here/installing-nuget">how to install Nuget Packages<a/>.
You may also take a look at the  Youtube Data API. It allows apps to retrieve and update YouTube content.
Your  app can use the YouTube Data API to fetch video feeds, channels, and playlists for videos that match particular criteria.

<h2>Description</h2>
<h4>1- Obtaining authorization credentials :</h4>
To use Youtube Data API V3, you need to have authorization credentianls.
In this sample, I used API Keys.
You can take a look on how to retrieve the keys <a target="_blank" href="https://developers.google.com/youtube/registering_an_application">here</a>.

<h4>2- Add the "YoutubeVideo" class :</h4>
<pre>
  <code>
  public class YoutubeVideo 
  { 
       public string Id { get; set; } 
       public string Title { get; set; } 
       public DateTime? PubDate { get; set; } 
       public string YoutubeLink { get; set; } 
       public string PlayerLink { get; set; } 
       public string Thumbnail { get; set; } 
       public string Description { get; set; } 
  }
  </code>
</pre>

YoutubeLink is the link on the youtube website (used to share the video).
PlayerLink is the link converted to be used on the MediaPlayer (MediaElement).

<h4>3- "GetChannelVideos" & "GetChannelVideosWithPagination" methods :</h4>
To add those methods, you need to install the Youtube Data API v3 nuget package.
This method has two parameters, the first one is the Channel ID, you can get it directly from Youtube or from the "GetChannelId" method.
I used the Search in Youtube Data API v3 to get the channel videos, you can read about it <a target="_blank" href="https://developers.google.com/youtube/v3/docs/search/list">here</a>.

<h4>4- "GetPlaylistVideos" method :</h4>
The Youtube playlists are managed by IDs as the channels.
You can take a look at PlaylistItems in Youtube Data API v3 <a target="_blank" href="https://developers.google.com/youtube/v3/docs/playlistItems/list">here</a>.

<h4>5- Retrieve the PlayerLink as the MediaPlayer source :</h4>
To get the PlayerLink, you need to install the Nuget Packages <a target="_blank" href="http://mytoolkit.codeplex.com/">MyToolkit</a> and <a target="_blank" href="http://mytoolkit.codeplex.com/">MyToolkitExtended</a> on your project.

<h3>That's it! I hope it was helplful.</h3>
