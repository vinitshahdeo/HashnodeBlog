## How to get GitHub Stars Contributions

Last year, GitHub launched the **GitHub Stars** [program](https://stars.github.com/) to thank GitHub’s most influential developers who have gone above and beyond in helping others in the community – **not only by maintaining repositories but by helping educate, inspire and influence others**.

[![github-star.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1620861295093/-z0eJTmdv.gif)](https://stars.github.com/profiles/vinitshahdeo/)

Be it blogs, podcasts, videos, community conferences or hackathons, [GitHub Stars](https://stars.github.com/profiles/) keep sharing their stories on the platform. **You can keep an eye on what's cooking on GitHub Star's pot!** 🌟 Wondering how? `github-stars-feed` is an open-sourced NPM [module](https://www.npmjs.com/package/github-stars-feed) that can help you in getting their latest feed. Now, it's open to your creativity, how you showcase their contributions in your application!


%[https://github.com/vinitshahdeo/github-stars-feed/]


## Here's how?

[![NPM](https://nodei.co/npm/github-stars-feed.png?compact=true)](https://www.npmjs.com/package/github-stars-feed)


- `npm init` your project
- `npm install github-stars-feed`
- `touch index.js`

Now you're just a couple of key-strokes away from getting the GitHub Stars feed in your `>_terminal`. It's time to utilize the most popular pair (`CTRL + C` and `CTRL + V`) among developers! Paste the below code-snippet inside `index.js` and run `node index.js`.

```js
const githubStars = require('github-stars-feed');

githubStars.getFeed((err, feed) => {
  if (err) {
    console.log('Something went wrong while fetching GitHub Stars Feed');
  } else {
    console.log(feed); // latest GitHub Stars contributions
  }
});
```

`getFeed()` will return a JSON response*(sample given below)* containing the latest [GitHub Stars](https://stars.github.com/profiles/) contributions.

```js

[
  {
    title: 'Meet Vinit Shahdeo, a resident of Jharkhand, has been recognized as a GitHub Star',
    summary: 'My journey got featured by the News Khajana.',
    link: 'https://thenewskhazana.com/story/meet-vinit-shahdeo-a-resident-of-jharkhand-has-been-recognized-as-a-github-star-22451/',
    updated: 'Sunday, November 3rd 2019',
    author: {
      name: 'vinitshahdeo',
      uri: 'https://stars.github.com/vinitshahdeo'
    }
  },
  {
    title: 'Mentor - Google Summer Of Code',
    summary: 'Postman is one of the mentoring organization for GSoC. This year, Postman has AsyncAPI Initiative as part of their team.\n\nI will be mentoring an idea for AsyncAPI i.e. AsyncDiff. It\'s basically a library to compare two AsyncAPI documents and generate diff for the review process.',
    link: 'https://community.postman.com/t/idea-9-asyncdiff-general-information/21694',
    updated: 'Sunday, November 3rd 2019',
    author: {
      name: 'vinitshahdeo',
      uri: 'https://stars.github.com/vinitshahdeo'
    }
  }
]
```

Additionally, you can provide `options` to filter the feed. Kindly refer [this](https://github.com/vinitshahdeo/github-stars-feed#options) for complete documentation.

```js
var options = {
  limit: 2,
  sanitize: true,
  username: 'vinitshahdeo'
};

githubStars.getFeed(options, (err, feed) => {
  if (err) {
    console.log('Something went wrong while fetching GitHub Stars Feed');
  } else {
    console.log(feed); // filtered feed
  }
});
```

> Please refer the [GitHub repository](https://github.com/vinitshahdeo/github-stars-feed) to explore more. 

Let me know what do you build consuming  [`github-stars-feed`](https://github.com/vinitshahdeo/github-stars-feed) on [Twitter](https://twitter.com/Vinit_Shahdeo).

[![Twitter Follow](https://img.shields.io/twitter/follow/Vinit_Shahdeo?style=social)](https://twitter.com/Vinit_Shahdeo)

---------

> I’m unbelievably humbled to have received an email saying ***“Congrats, you’re a GitHub Star!”*** back in March. From a (green) dot to a star, [here’s how my journey uncoiled](https://dev.to/vinitshahdeo/milepost-from-a-github-user-to-a-github-star-2o36)! 🚀

%[https://dev.to/vinitshahdeo/milepost-from-a-github-user-to-a-github-star-2o36]

🍻
Cheers:) 
