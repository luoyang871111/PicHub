# PicHub
GitHub图床
![91f9fdac5d634a1c4b6a3d819c855da5_1](https://github.com/luoyang871111/PicHub/assets/52514896/e7d838d7-40a7-46dd-b55b-7fdecaef5f15)


“Create or update file contents”的示例代码
Select the example type

Example for creating a file
PUT
/repos/{owner}/{repo}/contents/{path}
cURL
JavaScript

// Octokit.js
// https://github.com/octokit/core.js#readme
const octokit = new Octokit({
  auth: 'YOUR-TOKEN'
})

await octokit.request('PUT https://api.github.com/repos/luoyang871111/PicHub/contents/blue.png', {
  //owner: 'OWNER',
 //repo: 'REPO',
 //path: 'PATH',
  message: 'content内容为base64加密字符串,文本、图片、文件均为Base64加密字符串,图片访问域名https://luoyang871111.github.io/PicHub/blue.png,或者用download_url访问: https://raw.githubusercontent.com/luoyang871111/PicHub/main/blue.png',
  committer: {
    name: 'Micro',
    email: 'luoyang871111@github.com'
  },
  content: 'iVBORw0KGgoAAAANSUhEUgAAAIoAAACKCAYAAAB1h9JkAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAF1SURBVHhe7dYxAYAwEMDASgFR4LTYeyQ0Am44BxmyrmcPnAiFZN3vN3AiFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCITGzJEIhEQqJUEjMLIlQSIRCIhQSM0siFBKhkAiFxMySCIVEKCRCIdjzA5oVKWxK2iiRAAAAAElFTkSuQmCC',
  headers: {
    'X-GitHub-Api-Version': '2022-11-28'
  }
})


Response

示例响应
响应架构
Status: 201

{
    "content": {
        "name": "blue.png",
        "path": "blue.png",
        "sha": "151b5b8acb36161a831ff877e44c1bf81082a9a8",
        "size": 480,
        "url": "https://api.github.com/repos/luoyang871111/PicHub/contents/blue.png?ref=main",
        "html_url": "https://github.com/luoyang871111/PicHub/blob/main/blue.png",
        "git_url": "https://api.github.com/repos/luoyang871111/PicHub/git/blobs/151b5b8acb36161a831ff877e44c1bf81082a9a8",
        "download_url": "https://raw.githubusercontent.com/luoyang871111/PicHub/main/blue.png",
        "type": "file",
        "_links": {
            "self": "https://api.github.com/repos/luoyang871111/PicHub/contents/blue.png?ref=main",
            "git": "https://api.github.com/repos/luoyang871111/PicHub/git/blobs/151b5b8acb36161a831ff877e44c1bf81082a9a8",
            "html": "https://github.com/luoyang871111/PicHub/blob/main/blue.png"
        }
    },
    "commit": {
        "sha": "fe5c7959a54f445654f732ed21fa96121808982c",
        "node_id": "C_kwDOJ_5Iv9oAKGZlNWM3OTU5YTU0ZjQ0NTY1NGY3MzJlZDIxZmE5NjEyMTgwODk4MmM",
        "url": "https://api.github.com/repos/luoyang871111/PicHub/git/commits/fe5c7959a54f445654f732ed21fa96121808982c",
        "html_url": "https://github.com/luoyang871111/PicHub/commit/fe5c7959a54f445654f732ed21fa96121808982c",
        "author": {
            "name": "Micro",
            "email": "micro@abc.com",
            "date": "2023-07-28T07:35:26Z"
        },
        "committer": {
            "name": "Micro",
            "email": "micro@abc.com",
            "date": "2023-07-28T07:35:26Z"
        },
        "tree": {
            "sha": "ba5febce79b51afc2dceeaa2f96de964e9921859",
            "url": "https://api.github.com/repos/luoyang871111/PicHub/git/trees/ba5febce79b51afc2dceeaa2f96de964e9921859"
        },
        "message": "content内容为base64加密字符串,文本、图片、文件均为Base64加密字符串",
        "parents": [
            {
                "sha": "c88b33e72ec1cbb8134882b358da6c2a674fdb6e",
                "url": "https://api.github.com/repos/luoyang871111/PicHub/git/commits/c88b33e72ec1cbb8134882b358da6c2a674fdb6e",
                "html_url": "https://github.com/luoyang871111/PicHub/commit/c88b33e72ec1cbb8134882b358da6c2a674fdb6e"
            }
        ],
        "verification": {
            "verified": false,
            "reason": "unsigned",
            "signature": null,
            "payload": null
        }
    }
}

//content为Base64加密字符串 文字、图片、文件均是

blue.png为文件名
访问域名https://luoyang871111.github.io/PicHub/blue.png,
或者用download_url访问: https://raw.githubusercontent.com/luoyang871111/PicHub/main/blue.png
“Delete a file”的示例代码

DELETE
/repos/{owner}/{repo}/contents/{path}
cURL
JavaScript

// Octokit.js
// https://github.com/octokit/core.js#readme
const octokit = new Octokit({
  auth: 'YOUR-TOKEN'
})

await octokit.request('DELETE https://api.github.com/repos/luoyang871111/PicHub/contents/blue.png', {
  //owner: 'OWNER',
  //repo: 'REPO',
  //path: 'PATH',
  message: '删除提交对应到文件的网址以及sha值',
  committer: {
    name: 'Micro',
    email: 'luoyang871111@github.com'
  },
  sha: '151b5b8acb36161a831ff877e44c1bf81082a9a8',
  headers: {
    'X-GitHub-Api-Version': '2022-11-28'
  }
})
Response
响应架构
Status: 200

{
    "content": null,
    "commit": {
        "sha": "c88b33e72ec1cbb8134882b358da6c2a674fdb6e",
        "node_id": "C_kwDOJ_5Iv9oAKGM4OGIzM2U3MmVjMWNiYjgxMzQ4ODJiMzU4ZGE2YzJhNjc0ZmRiNmU",
        "url": "https://api.github.com/repos/luoyang871111/PicHub/git/commits/c88b33e72ec1cbb8134882b358da6c2a674fdb6e",
        "html_url": "https://github.com/luoyang871111/PicHub/commit/c88b33e72ec1cbb8134882b358da6c2a674fdb6e",
        "author": {
            "name": "Micro",
            "email": "micro@abc.com",
            "date": "2023-07-28T07:32:48Z"
        },
        "committer": {
            "name": "Micro",
            "email": "micro@abc.com",
            "date": "2023-07-28T07:32:48Z"
        },
        "tree": {
            "sha": "6e84478f42147c6e7044863d92c2c5b85a790587",
            "url": "https://api.github.com/repos/luoyang871111/PicHub/git/trees/6e84478f42147c6e7044863d92c2c5b85a790587"
        },
        "message": "content内容为base64加密字符串,文本、图片、文件均为Base64加密字符串",
        "parents": [
            {
                "sha": "64a07ab3062c9ac5f93206070d59fbbe386e9a92",
                "url": "https://api.github.com/repos/luoyang871111/PicHub/git/commits/64a07ab3062c9ac5f93206070d59fbbe386e9a92",
                "html_url": "https://github.com/luoyang871111/PicHub/commit/64a07ab3062c9ac5f93206070d59fbbe386e9a92"
            }
        ],
        "verification": {
            "verified": false,
            "reason": "unsigned",
            "signature": null,
            "payload": null
        }
    }
}![image](https://github.com/luoyang871111/PicHub/assets/52514896/eecfb33f-0591-4655-8b0f-dbdea2e2d874)
