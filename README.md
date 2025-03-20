# APP_Script
Mark All emails as  read.JS 

function markUnreadEmailsAsRead() {
  var threads = GmailApp.search("is:unread"); // Search for unread emails
  for (var i = 0; i < threads.length; i++) {
    threads[i].markRead(); // Mark as read
  }
  Logger.log("Marked " + threads.length + " unread emails as read.");
}
