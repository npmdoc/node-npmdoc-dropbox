# api documentation for  dropbox (v2.5.2)  [![npm package](https://img.shields.io/npm/v/npmdoc-dropbox.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dropbox) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dropbox.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dropbox)
#### The Dropbox JavaScript SDK is a lightweight, promise based interface to the Dropbox v2 API that works in both nodejs and browser environments.

[![NPM](https://nodei.co/npm/dropbox.png?downloads=true)](https://www.npmjs.com/package/dropbox)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-dropbox_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dropbox/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Riley Tomasek"
    },
    "bugs": {
        "url": "https://github.com/dropbox/dropbox-sdk-js/issues"
    },
    "dependencies": {
        "es6-promise": "^3.1.2",
        "superagent": "^1.8.3"
    },
    "description": "The Dropbox JavaScript SDK is a lightweight, promise based interface to the Dropbox v2 API that works in both nodejs and browser environments.",
    "devDependencies": {
        "chai": "^3.5.0",
        "eslint": "^2.7.0",
        "eslint-config-airbnb": "^6.2.0",
        "express": "^4.13.4",
        "express-urlrewrite": "^1.2.0",
        "gh-pages": "^0.11.0",
        "ink-docstrap": "^1.2.1",
        "jsdoc": "^3.4.0",
        "mocha": "^2.4.5",
        "pretty-bytes": "^2.0.1",
        "prompt": "^1.0.0",
        "sinon": "^1.17.3",
        "webpack": "^1.13.0",
        "webpack-dev-middleware": "^1.6.1"
    },
    "directories": {},
    "dist": {
        "shasum": "f058ee1818f46489f56cca19effabb88c9d9480c",
        "tarball": "https://registry.npmjs.org/dropbox/-/dropbox-2.5.2.tgz"
    },
    "files": [
        "*.md",
        "docs",
        "dist",
        "src"
    ],
    "gitHead": "f22f372f60f8df4fa147941ae880fbdddd34bf15",
    "keywords": [
        "dropbox",
        "files",
        "sync",
        "sdk",
        "client"
    ],
    "main": "src/index.js",
    "maintainers": [
        {
            "name": "kelkabany",
            "email": "ken@elkabany.com"
        },
        {
            "name": "praneshp",
            "email": "praneshpg@gmail.com"
        },
        {
            "name": "rileytomasek",
            "email": "riley.tomasek@gmail.com"
        }
    ],
    "name": "dropbox",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "dropbox/dropbox-sdk-js/issues"
    },
    "scripts": {
        "build": "npm run build-cjs && npm run build-umd && npm run compressed-size",
        "build-cjs": "webpack",
        "build-umd": "webpack -p --config webpack-umd.config.js",
        "compressed-size": "echo 'Dropbox-sdk.min.js gzipped will weigh' $(cat dist/Dropbox-sdk.min.js | gzip -9 | wc -c | pretty-bytes)",
        "generate-docs": "jsdoc -c ./conf.json -d generated-docs -t ./node_modules/ink-docstrap/template -R docs/README.md -r ./src",
        "lint": "eslint src --ignore-path src/types.js",
        "publish-docs": "rm -rf generated-docs && npm run generate-docs && gh-pages -d generated-docs",
        "start": "node examples/server.js",
        "test": "npm run lint && mocha 'test/*.js'"
    },
    "version": "2.5.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module dropbox](#apidoc.module.dropbox)
1.  [function <span class="apidocSignatureSpan">dropbox.</span>dropbox_base (options)](#apidoc.element.dropbox.dropbox_base)
1.  object <span class="apidocSignatureSpan">dropbox.</span>dropbox_base.prototype
1.  object <span class="apidocSignatureSpan">dropbox.</span>routes
1.  object <span class="apidocSignatureSpan">dropbox.</span>routes_team

#### [module dropbox.dropbox_base](#apidoc.module.dropbox.dropbox_base)
1.  [function <span class="apidocSignatureSpan">dropbox.</span>dropbox_base (options)](#apidoc.element.dropbox.dropbox_base.dropbox_base)

#### [module dropbox.dropbox_base.prototype](#apidoc.module.dropbox.dropbox_base.prototype)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getAccessToken ()](#apidoc.element.dropbox.dropbox_base.prototype.getAccessToken)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getAuthenticationUrl (redirectUri, state)](#apidoc.element.dropbox.dropbox_base.prototype.getAuthenticationUrl)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getClientId ()](#apidoc.element.dropbox.dropbox_base.prototype.getClientId)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getDownloadRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getDownloadRequest)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getRpcRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getRpcRequest)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getUploadRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getUploadRequest)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>request (path, args, auth, host, style)](#apidoc.element.dropbox.dropbox_base.prototype.request)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setAccessToken (accessToken)](#apidoc.element.dropbox.dropbox_base.prototype.setAccessToken)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setClientId (clientId)](#apidoc.element.dropbox.dropbox_base.prototype.setClientId)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setDownloadRequest (newDownloadRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setDownloadRequest)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setRpcRequest (newRpcRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setRpcRequest)
1.  [function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setUploadRequest (newUploadRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setUploadRequest)

#### [module dropbox.routes](#apidoc.module.dropbox.routes)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>authTokenFromOauth1 (arg)](#apidoc.element.dropbox.routes.authTokenFromOauth1)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>authTokenRevoke (arg)](#apidoc.element.dropbox.routes.authTokenRevoke)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesAlphaGetMetadata (arg)](#apidoc.element.dropbox.routes.filesAlphaGetMetadata)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesAlphaUpload (arg)](#apidoc.element.dropbox.routes.filesAlphaUpload)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopy (arg)](#apidoc.element.dropbox.routes.filesCopy)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyBatch (arg)](#apidoc.element.dropbox.routes.filesCopyBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyBatchCheck (arg)](#apidoc.element.dropbox.routes.filesCopyBatchCheck)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyReferenceGet (arg)](#apidoc.element.dropbox.routes.filesCopyReferenceGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyReferenceSave (arg)](#apidoc.element.dropbox.routes.filesCopyReferenceSave)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCreateFolder (arg)](#apidoc.element.dropbox.routes.filesCreateFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDelete (arg)](#apidoc.element.dropbox.routes.filesDelete)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDeleteBatch (arg)](#apidoc.element.dropbox.routes.filesDeleteBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDeleteBatchCheck (arg)](#apidoc.element.dropbox.routes.filesDeleteBatchCheck)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDownload (arg)](#apidoc.element.dropbox.routes.filesDownload)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetMetadata (arg)](#apidoc.element.dropbox.routes.filesGetMetadata)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetPreview (arg)](#apidoc.element.dropbox.routes.filesGetPreview)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetTemporaryLink (arg)](#apidoc.element.dropbox.routes.filesGetTemporaryLink)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetThumbnail (arg)](#apidoc.element.dropbox.routes.filesGetThumbnail)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolder (arg)](#apidoc.element.dropbox.routes.filesListFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderContinue (arg)](#apidoc.element.dropbox.routes.filesListFolderContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderGetLatestCursor (arg)](#apidoc.element.dropbox.routes.filesListFolderGetLatestCursor)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderLongpoll (arg)](#apidoc.element.dropbox.routes.filesListFolderLongpoll)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListRevisions (arg)](#apidoc.element.dropbox.routes.filesListRevisions)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMove (arg)](#apidoc.element.dropbox.routes.filesMove)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMoveBatch (arg)](#apidoc.element.dropbox.routes.filesMoveBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMoveBatchCheck (arg)](#apidoc.element.dropbox.routes.filesMoveBatchCheck)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPermanentlyDelete (arg)](#apidoc.element.dropbox.routes.filesPermanentlyDelete)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesAdd (arg)](#apidoc.element.dropbox.routes.filesPropertiesAdd)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesOverwrite (arg)](#apidoc.element.dropbox.routes.filesPropertiesOverwrite)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesRemove (arg)](#apidoc.element.dropbox.routes.filesPropertiesRemove)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesTemplateGet (arg)](#apidoc.element.dropbox.routes.filesPropertiesTemplateGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesTemplateList (arg)](#apidoc.element.dropbox.routes.filesPropertiesTemplateList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesUpdate (arg)](#apidoc.element.dropbox.routes.filesPropertiesUpdate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesRestore (arg)](#apidoc.element.dropbox.routes.filesRestore)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSaveUrl (arg)](#apidoc.element.dropbox.routes.filesSaveUrl)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSaveUrlCheckJobStatus (arg)](#apidoc.element.dropbox.routes.filesSaveUrlCheckJobStatus)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSearch (arg)](#apidoc.element.dropbox.routes.filesSearch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUpload (arg)](#apidoc.element.dropbox.routes.filesUpload)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionAppend (arg)](#apidoc.element.dropbox.routes.filesUploadSessionAppend)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionAppendV2 (arg)](#apidoc.element.dropbox.routes.filesUploadSessionAppendV2)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinish (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinish)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinishBatch (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinishBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinishBatchCheck (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinishBatchCheck)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionStart (arg)](#apidoc.element.dropbox.routes.filesUploadSessionStart)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsArchive (arg)](#apidoc.element.dropbox.routes.paperDocsArchive)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsDownload (arg)](#apidoc.element.dropbox.routes.paperDocsDownload)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsFolderUsersList (arg)](#apidoc.element.dropbox.routes.paperDocsFolderUsersList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsFolderUsersListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsFolderUsersListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsGetFolderInfo (arg)](#apidoc.element.dropbox.routes.paperDocsGetFolderInfo)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsList (arg)](#apidoc.element.dropbox.routes.paperDocsList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsPermanentlyDelete (arg)](#apidoc.element.dropbox.routes.paperDocsPermanentlyDelete)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsSharingPolicyGet (arg)](#apidoc.element.dropbox.routes.paperDocsSharingPolicyGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsSharingPolicySet (arg)](#apidoc.element.dropbox.routes.paperDocsSharingPolicySet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersAdd (arg)](#apidoc.element.dropbox.routes.paperDocsUsersAdd)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersList (arg)](#apidoc.element.dropbox.routes.paperDocsUsersList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsUsersListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersRemove (arg)](#apidoc.element.dropbox.routes.paperDocsUsersRemove)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingAddFileMember (arg)](#apidoc.element.dropbox.routes.sharingAddFileMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingAddFolderMember (arg)](#apidoc.element.dropbox.routes.sharingAddFolderMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingChangeFileMemberAccess (arg)](#apidoc.element.dropbox.routes.sharingChangeFileMemberAccess)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckJobStatus)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckRemoveMemberJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckRemoveMemberJobStatus)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckShareJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckShareJobStatus)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCreateSharedLink (arg)](#apidoc.element.dropbox.routes.sharingCreateSharedLink)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCreateSharedLinkWithSettings (arg)](#apidoc.element.dropbox.routes.sharingCreateSharedLinkWithSettings)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFileMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetFileMetadata)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFileMetadataBatch (arg)](#apidoc.element.dropbox.routes.sharingGetFileMetadataBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFolderMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetFolderMetadata)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinkFile (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinkFile)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinkMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinkMetadata)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinks (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinks)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembers (arg)](#apidoc.element.dropbox.routes.sharingListFileMembers)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembersBatch (arg)](#apidoc.element.dropbox.routes.sharingListFileMembersBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFileMembersContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolderMembers (arg)](#apidoc.element.dropbox.routes.sharingListFolderMembers)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolderMembersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFolderMembersContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolders (arg)](#apidoc.element.dropbox.routes.sharingListFolders)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFoldersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFoldersContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListMountableFolders (arg)](#apidoc.element.dropbox.routes.sharingListMountableFolders)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListMountableFoldersContinue (arg)](#apidoc.element.dropbox.routes.sharingListMountableFoldersContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListReceivedFiles (arg)](#apidoc.element.dropbox.routes.sharingListReceivedFiles)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListReceivedFilesContinue (arg)](#apidoc.element.dropbox.routes.sharingListReceivedFilesContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListSharedLinks (arg)](#apidoc.element.dropbox.routes.sharingListSharedLinks)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingModifySharedLinkSettings (arg)](#apidoc.element.dropbox.routes.sharingModifySharedLinkSettings)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingMountFolder (arg)](#apidoc.element.dropbox.routes.sharingMountFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRelinquishFileMembership (arg)](#apidoc.element.dropbox.routes.sharingRelinquishFileMembership)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRelinquishFolderMembership (arg)](#apidoc.element.dropbox.routes.sharingRelinquishFolderMembership)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFileMember (arg)](#apidoc.element.dropbox.routes.sharingRemoveFileMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFileMember2 (arg)](#apidoc.element.dropbox.routes.sharingRemoveFileMember2)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFolderMember (arg)](#apidoc.element.dropbox.routes.sharingRemoveFolderMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRevokeSharedLink (arg)](#apidoc.element.dropbox.routes.sharingRevokeSharedLink)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingShareFolder (arg)](#apidoc.element.dropbox.routes.sharingShareFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingTransferFolder (arg)](#apidoc.element.dropbox.routes.sharingTransferFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnmountFolder (arg)](#apidoc.element.dropbox.routes.sharingUnmountFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnshareFile (arg)](#apidoc.element.dropbox.routes.sharingUnshareFile)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnshareFolder (arg)](#apidoc.element.dropbox.routes.sharingUnshareFolder)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFileMember (arg)](#apidoc.element.dropbox.routes.sharingUpdateFileMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFolderMember (arg)](#apidoc.element.dropbox.routes.sharingUpdateFolderMember)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFolderPolicy (arg)](#apidoc.element.dropbox.routes.sharingUpdateFolderPolicy)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetAccount (arg)](#apidoc.element.dropbox.routes.usersGetAccount)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetAccountBatch (arg)](#apidoc.element.dropbox.routes.usersGetAccountBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetCurrentAccount (arg)](#apidoc.element.dropbox.routes.usersGetCurrentAccount)
1.  [function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetSpaceUsage (arg)](#apidoc.element.dropbox.routes.usersGetSpaceUsage)

#### [module dropbox.routes_team](#apidoc.module.dropbox.routes_team)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListMemberDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListMemberDevices)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListMembersDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListMembersDevices)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListTeamDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListTeamDevices)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesRevokeDeviceSession (arg)](#apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSession)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesRevokeDeviceSessionBatch (arg)](#apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSessionBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamGetInfo)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsCreate (arg)](#apidoc.element.dropbox.routes_team.teamGroupsCreate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsDelete (arg)](#apidoc.element.dropbox.routes_team.teamGroupsDelete)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamGroupsGetInfo)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamGroupsJobStatusGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsList (arg)](#apidoc.element.dropbox.routes_team.teamGroupsList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsListContinue (arg)](#apidoc.element.dropbox.routes_team.teamGroupsListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersAdd (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersAdd)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersList (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersListContinue (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersRemove (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersRemove)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersSetAccessType (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersSetAccessType)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsUpdate (arg)](#apidoc.element.dropbox.routes_team.teamGroupsUpdate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListMemberLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListMemberLinkedApps)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListMembersLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListMembersLinkedApps)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListTeamLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListTeamLinkedApps)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsRevokeLinkedApp (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedApp)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsRevokeLinkedAppBatch (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedAppBatch)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersAdd (arg)](#apidoc.element.dropbox.routes_team.teamMembersAdd)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersAddJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamMembersAddJobStatusGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamMembersGetInfo)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersList (arg)](#apidoc.element.dropbox.routes_team.teamMembersList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersListContinue (arg)](#apidoc.element.dropbox.routes_team.teamMembersListContinue)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRecover (arg)](#apidoc.element.dropbox.routes_team.teamMembersRecover)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRemove (arg)](#apidoc.element.dropbox.routes_team.teamMembersRemove)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRemoveJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamMembersRemoveJobStatusGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSendWelcomeEmail (arg)](#apidoc.element.dropbox.routes_team.teamMembersSendWelcomeEmail)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSetAdminPermissions (arg)](#apidoc.element.dropbox.routes_team.teamMembersSetAdminPermissions)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSetProfile (arg)](#apidoc.element.dropbox.routes_team.teamMembersSetProfile)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSuspend (arg)](#apidoc.element.dropbox.routes_team.teamMembersSuspend)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersUnsuspend (arg)](#apidoc.element.dropbox.routes_team.teamMembersUnsuspend)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateAdd (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateAdd)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateGet (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateGet)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateList (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateUpdate (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateUpdate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetActivity (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetActivity)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetDevices (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetDevices)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetMembership (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetMembership)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetStorage (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetStorage)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderActivate (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderActivate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderArchive (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderArchive)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderArchiveCheck (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderArchiveCheck)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderCreate (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderCreate)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderGetInfo)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderList (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderList)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderPermanentlyDelete (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderPermanentlyDelete)
1.  [function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderRename (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderRename)



# <a name="apidoc.module.dropbox"></a>[module dropbox](#apidoc.module.dropbox)

#### <a name="apidoc.element.dropbox.dropbox_base"></a>[function <span class="apidocSignatureSpan">dropbox.</span>dropbox_base (options)](#apidoc.element.dropbox.dropbox_base)
- description and source-code
```javascript
dropbox_base = function (options) {
  options = options || {};
  this.accessToken = options.accessToken;
  this.clientId = options.clientId;
  this.selectUser = options.selectUser;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dropbox.dropbox_base"></a>[module dropbox.dropbox_base](#apidoc.module.dropbox.dropbox_base)

#### <a name="apidoc.element.dropbox.dropbox_base.dropbox_base"></a>[function <span class="apidocSignatureSpan">dropbox.</span>dropbox_base (options)](#apidoc.element.dropbox.dropbox_base.dropbox_base)
- description and source-code
```javascript
dropbox_base = function (options) {
  options = options || {};
  this.accessToken = options.accessToken;
  this.clientId = options.clientId;
  this.selectUser = options.selectUser;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dropbox.dropbox_base.prototype"></a>[module dropbox.dropbox_base.prototype](#apidoc.module.dropbox.dropbox_base.prototype)

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getAccessToken"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getAccessToken ()](#apidoc.element.dropbox.dropbox_base.prototype.getAccessToken)
- description and source-code
```javascript
getAccessToken = function () {
  return this.accessToken;
}
```
- example usage
```shell
...
    case REQUEST_CONSTANTS.UPLOAD:
      request = this.getUploadRequest();
      break;
    default:
      throw new Error('Invalid request style: ' + style);
  }

  return request(path, args, auth, host, this.getAccessToken(), this.selectUser);
};

DropboxBase.prototype.setRpcRequest = function (newRpcRequest) {
  DropboxBase.prototype.rpcRequest = newRpcRequest;
};

DropboxBase.prototype.getRpcRequest = function () {
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getAuthenticationUrl"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getAuthenticationUrl (redirectUri, state)](#apidoc.element.dropbox.dropbox_base.prototype.getAuthenticationUrl)
- description and source-code
```javascript
getAuthenticationUrl = function (redirectUri, state) {
  var AUTH_BASE_URL = 'https://www.dropbox.com/oauth2/authorize';
  var clientId = this.getClientId();
  var authUrl;
  if (!clientId) {
    throw new Error('A client id is required. You can set the client id using .setClientId().');
  }
  if (!redirectUri) {
    throw new Error('A redirect uri is required.');
  }

  authUrl = AUTH_BASE_URL + '?response_type=token&client_id=' + clientId;
  if (redirectUri) {
    authUrl = authUrl + '&redirect_uri=' + redirectUri;
  }
  if (state) {
    authUrl = authUrl + '&state=' + state;
  }
  return authUrl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getClientId"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getClientId ()](#apidoc.element.dropbox.dropbox_base.prototype.getClientId)
- description and source-code
```javascript
getClientId = function () {
  return this.clientId;
}
```
- example usage
```shell
...
 * authenticating. This must be added to your app through the admin interface.
 * @arg {String} [state] - State that will be returned in the redirect URL to help
 * prevent cross site scripting attacks.
 * @returns {String} Url to send user to for Dropbox API authentication
 */
DropboxBase.prototype.getAuthenticationUrl = function (redirectUri, state) {
var AUTH_BASE_URL = 'https://www.dropbox.com/oauth2/authorize';
var clientId = this.getClientId();
var authUrl;
if (!clientId) {
  throw new Error('A client id is required. You can set the client id using .setClientId().');
}
if (!redirectUri) {
  throw new Error('A redirect uri is required.');
}
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getDownloadRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getDownloadRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getDownloadRequest)
- description and source-code
```javascript
getDownloadRequest = function () {
  if (DropboxBase.prototype.downloadRequest === undefined) {
    DropboxBase.prototype.downloadRequest = require('./download-request');
  }

  return DropboxBase.prototype.downloadRequest;
}
```
- example usage
```shell
...
DropboxBase.prototype.request = function (path, args, auth, host, style) {
var request = null;
switch (style) {
  case REQUEST_CONSTANTS.RPC:
    request = this.getRpcRequest();
    break;
  case REQUEST_CONSTANTS.DOWNLOAD:
    request = this.getDownloadRequest();
    break;
  case REQUEST_CONSTANTS.UPLOAD:
    request = this.getUploadRequest();
    break;
  default:
    throw new Error('Invalid request style: ' + style);
}
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getRpcRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getRpcRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getRpcRequest)
- description and source-code
```javascript
getRpcRequest = function () {
  if (DropboxBase.prototype.rpcRequest === undefined) {
    DropboxBase.prototype.rpcRequest = require('./rpc-request');
  }

  return DropboxBase.prototype.rpcRequest;
}
```
- example usage
```shell
...
return authUrl;
};

DropboxBase.prototype.request = function (path, args, auth, host, style) {
var request = null;
switch (style) {
  case REQUEST_CONSTANTS.RPC:
    request = this.getRpcRequest();
    break;
  case REQUEST_CONSTANTS.DOWNLOAD:
    request = this.getDownloadRequest();
    break;
  case REQUEST_CONSTANTS.UPLOAD:
    request = this.getUploadRequest();
    break;
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.getUploadRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>getUploadRequest ()](#apidoc.element.dropbox.dropbox_base.prototype.getUploadRequest)
- description and source-code
```javascript
getUploadRequest = function () {
  if (DropboxBase.prototype.uploadRequest === undefined) {
    DropboxBase.prototype.uploadRequest = require('./upload-request');
  }

  return DropboxBase.prototype.uploadRequest;
}
```
- example usage
```shell
...
    case REQUEST_CONSTANTS.RPC:
      request = this.getRpcRequest();
      break;
    case REQUEST_CONSTANTS.DOWNLOAD:
      request = this.getDownloadRequest();
      break;
    case REQUEST_CONSTANTS.UPLOAD:
      request = this.getUploadRequest();
      break;
    default:
      throw new Error('Invalid request style: ' + style);
  }

  return request(path, args, auth, host, this.getAccessToken(), this.selectUser);
};
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.request"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>request (path, args, auth, host, style)](#apidoc.element.dropbox.dropbox_base.prototype.request)
- description and source-code
```javascript
request = function (path, args, auth, host, style) {
  var request = null;
  switch (style) {
    case REQUEST_CONSTANTS.RPC:
      request = this.getRpcRequest();
      break;
    case REQUEST_CONSTANTS.DOWNLOAD:
      request = this.getDownloadRequest();
      break;
    case REQUEST_CONSTANTS.UPLOAD:
      request = this.getUploadRequest();
      break;
    default:
      throw new Error('Invalid request style: ' + style);
  }

  return request(path, args, auth, host, this.getAccessToken(), this.selectUser);
}
```
- example usage
```shell
...
/**
* List all device sessions of a team's member.
* @function DropboxTeam#teamDevicesListMemberDevices
* @arg {TeamListMemberDevicesArg} arg - The request parameters.
* @returns {Promise.<TeamListMemberDevicesResult, Error.<TeamListMemberDevicesError>>}
*/
routes.teamDevicesListMemberDevices = function (arg) {
 return this.request('team/devices/list_member_devices', arg, 'team', 'api', 'rpc');
};

/**
* List all device sessions of a team.
* @function DropboxTeam#teamDevicesListMembersDevices
* @arg {TeamListMembersDevicesArg} arg - The request parameters.
* @returns {Promise.<TeamListMembersDevicesResult, Error.<TeamListMembersDevicesError>>}
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.setAccessToken"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setAccessToken (accessToken)](#apidoc.element.dropbox.dropbox_base.prototype.setAccessToken)
- description and source-code
```javascript
setAccessToken = function (accessToken) {
  this.accessToken = accessToken;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.setClientId"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setClientId (clientId)](#apidoc.element.dropbox.dropbox_base.prototype.setClientId)
- description and source-code
```javascript
setClientId = function (clientId) {
  this.clientId = clientId;
}
```
- example usage
```shell
...
 * @returns {String} Url to send user to for Dropbox API authentication
 */
DropboxBase.prototype.getAuthenticationUrl = function (redirectUri, state) {
var AUTH_BASE_URL = 'https://www.dropbox.com/oauth2/authorize';
var clientId = this.getClientId();
var authUrl;
if (!clientId) {
  throw new Error('A client id is required. You can set the client id using .setClientId().');
}
if (!redirectUri) {
  throw new Error('A redirect uri is required.');
}

authUrl = AUTH_BASE_URL + '?response_type=token&client_id=' + clientId;
if (redirectUri) {
...
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.setDownloadRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setDownloadRequest (newDownloadRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setDownloadRequest)
- description and source-code
```javascript
setDownloadRequest = function (newDownloadRequest) {
  DropboxBase.prototype.downloadRequest = newDownloadRequest;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.setRpcRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setRpcRequest (newRpcRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setRpcRequest)
- description and source-code
```javascript
setRpcRequest = function (newRpcRequest) {
  DropboxBase.prototype.rpcRequest = newRpcRequest;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.dropbox_base.prototype.setUploadRequest"></a>[function <span class="apidocSignatureSpan">dropbox.dropbox_base.prototype.</span>setUploadRequest (newUploadRequest)](#apidoc.element.dropbox.dropbox_base.prototype.setUploadRequest)
- description and source-code
```javascript
setUploadRequest = function (newUploadRequest) {
  DropboxBase.prototype.uploadRequest = newUploadRequest;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dropbox.routes"></a>[module dropbox.routes](#apidoc.module.dropbox.routes)

#### <a name="apidoc.element.dropbox.routes.authTokenFromOauth1"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>authTokenFromOauth1 (arg)](#apidoc.element.dropbox.routes.authTokenFromOauth1)
- description and source-code
```javascript
authTokenFromOauth1 = function (arg) {
  return this.request('auth/token/from_oauth1', arg, 'app', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.authTokenRevoke"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>authTokenRevoke (arg)](#apidoc.element.dropbox.routes.authTokenRevoke)
- description and source-code
```javascript
authTokenRevoke = function (arg) {
  return this.request('auth/token/revoke', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesAlphaGetMetadata"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesAlphaGetMetadata (arg)](#apidoc.element.dropbox.routes.filesAlphaGetMetadata)
- description and source-code
```javascript
filesAlphaGetMetadata = function (arg) {
  return this.request('files/alpha/get_metadata', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesAlphaUpload"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesAlphaUpload (arg)](#apidoc.element.dropbox.routes.filesAlphaUpload)
- description and source-code
```javascript
filesAlphaUpload = function (arg) {
  return this.request('files/alpha/upload', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCopy"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopy (arg)](#apidoc.element.dropbox.routes.filesCopy)
- description and source-code
```javascript
filesCopy = function (arg) {
  return this.request('files/copy', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCopyBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyBatch (arg)](#apidoc.element.dropbox.routes.filesCopyBatch)
- description and source-code
```javascript
filesCopyBatch = function (arg) {
  return this.request('files/copy_batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCopyBatchCheck"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyBatchCheck (arg)](#apidoc.element.dropbox.routes.filesCopyBatchCheck)
- description and source-code
```javascript
filesCopyBatchCheck = function (arg) {
  return this.request('files/copy_batch/check', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCopyReferenceGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyReferenceGet (arg)](#apidoc.element.dropbox.routes.filesCopyReferenceGet)
- description and source-code
```javascript
filesCopyReferenceGet = function (arg) {
  return this.request('files/copy_reference/get', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCopyReferenceSave"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCopyReferenceSave (arg)](#apidoc.element.dropbox.routes.filesCopyReferenceSave)
- description and source-code
```javascript
filesCopyReferenceSave = function (arg) {
  return this.request('files/copy_reference/save', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesCreateFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesCreateFolder (arg)](#apidoc.element.dropbox.routes.filesCreateFolder)
- description and source-code
```javascript
filesCreateFolder = function (arg) {
  return this.request('files/create_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesDelete"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDelete (arg)](#apidoc.element.dropbox.routes.filesDelete)
- description and source-code
```javascript
filesDelete = function (arg) {
  return this.request('files/delete', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesDeleteBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDeleteBatch (arg)](#apidoc.element.dropbox.routes.filesDeleteBatch)
- description and source-code
```javascript
filesDeleteBatch = function (arg) {
  return this.request('files/delete_batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesDeleteBatchCheck"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDeleteBatchCheck (arg)](#apidoc.element.dropbox.routes.filesDeleteBatchCheck)
- description and source-code
```javascript
filesDeleteBatchCheck = function (arg) {
  return this.request('files/delete_batch/check', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesDownload"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesDownload (arg)](#apidoc.element.dropbox.routes.filesDownload)
- description and source-code
```javascript
filesDownload = function (arg) {
  return this.request('files/download', arg, 'user', 'content', 'download');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesGetMetadata"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetMetadata (arg)](#apidoc.element.dropbox.routes.filesGetMetadata)
- description and source-code
```javascript
filesGetMetadata = function (arg) {
  return this.request('files/get_metadata', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesGetPreview"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetPreview (arg)](#apidoc.element.dropbox.routes.filesGetPreview)
- description and source-code
```javascript
filesGetPreview = function (arg) {
  return this.request('files/get_preview', arg, 'user', 'content', 'download');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesGetTemporaryLink"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetTemporaryLink (arg)](#apidoc.element.dropbox.routes.filesGetTemporaryLink)
- description and source-code
```javascript
filesGetTemporaryLink = function (arg) {
  return this.request('files/get_temporary_link', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesGetThumbnail"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesGetThumbnail (arg)](#apidoc.element.dropbox.routes.filesGetThumbnail)
- description and source-code
```javascript
filesGetThumbnail = function (arg) {
  return this.request('files/get_thumbnail', arg, 'user', 'content', 'download');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesListFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolder (arg)](#apidoc.element.dropbox.routes.filesListFolder)
- description and source-code
```javascript
filesListFolder = function (arg) {
  return this.request('files/list_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
...

Use with a module bundler like
[webpack](https://github.com/webpack/webpack) or
[browserify](http://browserify.org/):
'''javascript
var Dropbox = require('dropbox');
var dbx = new Dropbox({ accessToken: 'YOUR_ACCESS_TOKEN_HERE' });
dbx.filesListFolder({path: ''})
  .then(function(response) {
    console.log(response);
  })
  .catch(function(error) {
    console.log(error);
  });
'''
...
```

#### <a name="apidoc.element.dropbox.routes.filesListFolderContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderContinue (arg)](#apidoc.element.dropbox.routes.filesListFolderContinue)
- description and source-code
```javascript
filesListFolderContinue = function (arg) {
  return this.request('files/list_folder/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesListFolderGetLatestCursor"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderGetLatestCursor (arg)](#apidoc.element.dropbox.routes.filesListFolderGetLatestCursor)
- description and source-code
```javascript
filesListFolderGetLatestCursor = function (arg) {
  return this.request('files/list_folder/get_latest_cursor', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesListFolderLongpoll"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListFolderLongpoll (arg)](#apidoc.element.dropbox.routes.filesListFolderLongpoll)
- description and source-code
```javascript
filesListFolderLongpoll = function (arg) {
  return this.request('files/list_folder/longpoll', arg, 'noauth', 'notify', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesListRevisions"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesListRevisions (arg)](#apidoc.element.dropbox.routes.filesListRevisions)
- description and source-code
```javascript
filesListRevisions = function (arg) {
  return this.request('files/list_revisions', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesMove"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMove (arg)](#apidoc.element.dropbox.routes.filesMove)
- description and source-code
```javascript
filesMove = function (arg) {
  return this.request('files/move', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesMoveBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMoveBatch (arg)](#apidoc.element.dropbox.routes.filesMoveBatch)
- description and source-code
```javascript
filesMoveBatch = function (arg) {
  return this.request('files/move_batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesMoveBatchCheck"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesMoveBatchCheck (arg)](#apidoc.element.dropbox.routes.filesMoveBatchCheck)
- description and source-code
```javascript
filesMoveBatchCheck = function (arg) {
  return this.request('files/move_batch/check', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPermanentlyDelete"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPermanentlyDelete (arg)](#apidoc.element.dropbox.routes.filesPermanentlyDelete)
- description and source-code
```javascript
filesPermanentlyDelete = function (arg) {
  return this.request('files/permanently_delete', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesAdd"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesAdd (arg)](#apidoc.element.dropbox.routes.filesPropertiesAdd)
- description and source-code
```javascript
filesPropertiesAdd = function (arg) {
  return this.request('files/properties/add', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesOverwrite"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesOverwrite (arg)](#apidoc.element.dropbox.routes.filesPropertiesOverwrite)
- description and source-code
```javascript
filesPropertiesOverwrite = function (arg) {
  return this.request('files/properties/overwrite', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesRemove"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesRemove (arg)](#apidoc.element.dropbox.routes.filesPropertiesRemove)
- description and source-code
```javascript
filesPropertiesRemove = function (arg) {
  return this.request('files/properties/remove', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesTemplateGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesTemplateGet (arg)](#apidoc.element.dropbox.routes.filesPropertiesTemplateGet)
- description and source-code
```javascript
filesPropertiesTemplateGet = function (arg) {
  return this.request('files/properties/template/get', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesTemplateList"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesTemplateList (arg)](#apidoc.element.dropbox.routes.filesPropertiesTemplateList)
- description and source-code
```javascript
filesPropertiesTemplateList = function (arg) {
  return this.request('files/properties/template/list', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesPropertiesUpdate"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesPropertiesUpdate (arg)](#apidoc.element.dropbox.routes.filesPropertiesUpdate)
- description and source-code
```javascript
filesPropertiesUpdate = function (arg) {
  return this.request('files/properties/update', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesRestore"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesRestore (arg)](#apidoc.element.dropbox.routes.filesRestore)
- description and source-code
```javascript
filesRestore = function (arg) {
  return this.request('files/restore', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesSaveUrl"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSaveUrl (arg)](#apidoc.element.dropbox.routes.filesSaveUrl)
- description and source-code
```javascript
filesSaveUrl = function (arg) {
  return this.request('files/save_url', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesSaveUrlCheckJobStatus"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSaveUrlCheckJobStatus (arg)](#apidoc.element.dropbox.routes.filesSaveUrlCheckJobStatus)
- description and source-code
```javascript
filesSaveUrlCheckJobStatus = function (arg) {
  return this.request('files/save_url/check_job_status', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesSearch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesSearch (arg)](#apidoc.element.dropbox.routes.filesSearch)
- description and source-code
```javascript
filesSearch = function (arg) {
  return this.request('files/search', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUpload"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUpload (arg)](#apidoc.element.dropbox.routes.filesUpload)
- description and source-code
```javascript
filesUpload = function (arg) {
  return this.request('files/upload', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionAppend"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionAppend (arg)](#apidoc.element.dropbox.routes.filesUploadSessionAppend)
- description and source-code
```javascript
filesUploadSessionAppend = function (arg) {
  return this.request('files/upload_session/append', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionAppendV2"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionAppendV2 (arg)](#apidoc.element.dropbox.routes.filesUploadSessionAppendV2)
- description and source-code
```javascript
filesUploadSessionAppendV2 = function (arg) {
  return this.request('files/upload_session/append_v2', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionFinish"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinish (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinish)
- description and source-code
```javascript
filesUploadSessionFinish = function (arg) {
  return this.request('files/upload_session/finish', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionFinishBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinishBatch (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinishBatch)
- description and source-code
```javascript
filesUploadSessionFinishBatch = function (arg) {
  return this.request('files/upload_session/finish_batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionFinishBatchCheck"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionFinishBatchCheck (arg)](#apidoc.element.dropbox.routes.filesUploadSessionFinishBatchCheck)
- description and source-code
```javascript
filesUploadSessionFinishBatchCheck = function (arg) {
  return this.request('files/upload_session/finish_batch/check', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.filesUploadSessionStart"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>filesUploadSessionStart (arg)](#apidoc.element.dropbox.routes.filesUploadSessionStart)
- description and source-code
```javascript
filesUploadSessionStart = function (arg) {
  return this.request('files/upload_session/start', arg, 'user', 'content', 'upload');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsArchive"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsArchive (arg)](#apidoc.element.dropbox.routes.paperDocsArchive)
- description and source-code
```javascript
paperDocsArchive = function (arg) {
  return this.request('paper/docs/archive', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsDownload"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsDownload (arg)](#apidoc.element.dropbox.routes.paperDocsDownload)
- description and source-code
```javascript
paperDocsDownload = function (arg) {
  return this.request('paper/docs/download', arg, 'user', 'api', 'download');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsFolderUsersList"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsFolderUsersList (arg)](#apidoc.element.dropbox.routes.paperDocsFolderUsersList)
- description and source-code
```javascript
paperDocsFolderUsersList = function (arg) {
  return this.request('paper/docs/folder_users/list', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsFolderUsersListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsFolderUsersListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsFolderUsersListContinue)
- description and source-code
```javascript
paperDocsFolderUsersListContinue = function (arg) {
  return this.request('paper/docs/folder_users/list/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsGetFolderInfo"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsGetFolderInfo (arg)](#apidoc.element.dropbox.routes.paperDocsGetFolderInfo)
- description and source-code
```javascript
paperDocsGetFolderInfo = function (arg) {
  return this.request('paper/docs/get_folder_info', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsList"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsList (arg)](#apidoc.element.dropbox.routes.paperDocsList)
- description and source-code
```javascript
paperDocsList = function (arg) {
  return this.request('paper/docs/list', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsListContinue)
- description and source-code
```javascript
paperDocsListContinue = function (arg) {
  return this.request('paper/docs/list/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsPermanentlyDelete"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsPermanentlyDelete (arg)](#apidoc.element.dropbox.routes.paperDocsPermanentlyDelete)
- description and source-code
```javascript
paperDocsPermanentlyDelete = function (arg) {
  return this.request('paper/docs/permanently_delete', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsSharingPolicyGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsSharingPolicyGet (arg)](#apidoc.element.dropbox.routes.paperDocsSharingPolicyGet)
- description and source-code
```javascript
paperDocsSharingPolicyGet = function (arg) {
  return this.request('paper/docs/sharing_policy/get', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsSharingPolicySet"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsSharingPolicySet (arg)](#apidoc.element.dropbox.routes.paperDocsSharingPolicySet)
- description and source-code
```javascript
paperDocsSharingPolicySet = function (arg) {
  return this.request('paper/docs/sharing_policy/set', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsUsersAdd"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersAdd (arg)](#apidoc.element.dropbox.routes.paperDocsUsersAdd)
- description and source-code
```javascript
paperDocsUsersAdd = function (arg) {
  return this.request('paper/docs/users/add', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsUsersList"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersList (arg)](#apidoc.element.dropbox.routes.paperDocsUsersList)
- description and source-code
```javascript
paperDocsUsersList = function (arg) {
  return this.request('paper/docs/users/list', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsUsersListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersListContinue (arg)](#apidoc.element.dropbox.routes.paperDocsUsersListContinue)
- description and source-code
```javascript
paperDocsUsersListContinue = function (arg) {
  return this.request('paper/docs/users/list/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.paperDocsUsersRemove"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>paperDocsUsersRemove (arg)](#apidoc.element.dropbox.routes.paperDocsUsersRemove)
- description and source-code
```javascript
paperDocsUsersRemove = function (arg) {
  return this.request('paper/docs/users/remove', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingAddFileMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingAddFileMember (arg)](#apidoc.element.dropbox.routes.sharingAddFileMember)
- description and source-code
```javascript
sharingAddFileMember = function (arg) {
  return this.request('sharing/add_file_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingAddFolderMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingAddFolderMember (arg)](#apidoc.element.dropbox.routes.sharingAddFolderMember)
- description and source-code
```javascript
sharingAddFolderMember = function (arg) {
  return this.request('sharing/add_folder_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingChangeFileMemberAccess"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingChangeFileMemberAccess (arg)](#apidoc.element.dropbox.routes.sharingChangeFileMemberAccess)
- description and source-code
```javascript
sharingChangeFileMemberAccess = function (arg) {
  return this.request('sharing/change_file_member_access', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingCheckJobStatus"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckJobStatus)
- description and source-code
```javascript
sharingCheckJobStatus = function (arg) {
  return this.request('sharing/check_job_status', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingCheckRemoveMemberJobStatus"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckRemoveMemberJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckRemoveMemberJobStatus)
- description and source-code
```javascript
sharingCheckRemoveMemberJobStatus = function (arg) {
  return this.request('sharing/check_remove_member_job_status', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingCheckShareJobStatus"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCheckShareJobStatus (arg)](#apidoc.element.dropbox.routes.sharingCheckShareJobStatus)
- description and source-code
```javascript
sharingCheckShareJobStatus = function (arg) {
  return this.request('sharing/check_share_job_status', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingCreateSharedLink"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCreateSharedLink (arg)](#apidoc.element.dropbox.routes.sharingCreateSharedLink)
- description and source-code
```javascript
sharingCreateSharedLink = function (arg) {
  return this.request('sharing/create_shared_link', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingCreateSharedLinkWithSettings"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingCreateSharedLinkWithSettings (arg)](#apidoc.element.dropbox.routes.sharingCreateSharedLinkWithSettings)
- description and source-code
```javascript
sharingCreateSharedLinkWithSettings = function (arg) {
  return this.request('sharing/create_shared_link_with_settings', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetFileMetadata"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFileMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetFileMetadata)
- description and source-code
```javascript
sharingGetFileMetadata = function (arg) {
  return this.request('sharing/get_file_metadata', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetFileMetadataBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFileMetadataBatch (arg)](#apidoc.element.dropbox.routes.sharingGetFileMetadataBatch)
- description and source-code
```javascript
sharingGetFileMetadataBatch = function (arg) {
  return this.request('sharing/get_file_metadata/batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetFolderMetadata"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetFolderMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetFolderMetadata)
- description and source-code
```javascript
sharingGetFolderMetadata = function (arg) {
  return this.request('sharing/get_folder_metadata', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetSharedLinkFile"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinkFile (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinkFile)
- description and source-code
```javascript
sharingGetSharedLinkFile = function (arg) {
  return this.request('sharing/get_shared_link_file', arg, 'user', 'content', 'download');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetSharedLinkMetadata"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinkMetadata (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinkMetadata)
- description and source-code
```javascript
sharingGetSharedLinkMetadata = function (arg) {
  return this.request('sharing/get_shared_link_metadata', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingGetSharedLinks"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingGetSharedLinks (arg)](#apidoc.element.dropbox.routes.sharingGetSharedLinks)
- description and source-code
```javascript
sharingGetSharedLinks = function (arg) {
  return this.request('sharing/get_shared_links', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFileMembers"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembers (arg)](#apidoc.element.dropbox.routes.sharingListFileMembers)
- description and source-code
```javascript
sharingListFileMembers = function (arg) {
  return this.request('sharing/list_file_members', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFileMembersBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembersBatch (arg)](#apidoc.element.dropbox.routes.sharingListFileMembersBatch)
- description and source-code
```javascript
sharingListFileMembersBatch = function (arg) {
  return this.request('sharing/list_file_members/batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFileMembersContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFileMembersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFileMembersContinue)
- description and source-code
```javascript
sharingListFileMembersContinue = function (arg) {
  return this.request('sharing/list_file_members/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFolderMembers"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolderMembers (arg)](#apidoc.element.dropbox.routes.sharingListFolderMembers)
- description and source-code
```javascript
sharingListFolderMembers = function (arg) {
  return this.request('sharing/list_folder_members', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFolderMembersContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolderMembersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFolderMembersContinue)
- description and source-code
```javascript
sharingListFolderMembersContinue = function (arg) {
  return this.request('sharing/list_folder_members/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFolders"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFolders (arg)](#apidoc.element.dropbox.routes.sharingListFolders)
- description and source-code
```javascript
sharingListFolders = function (arg) {
  return this.request('sharing/list_folders', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListFoldersContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListFoldersContinue (arg)](#apidoc.element.dropbox.routes.sharingListFoldersContinue)
- description and source-code
```javascript
sharingListFoldersContinue = function (arg) {
  return this.request('sharing/list_folders/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListMountableFolders"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListMountableFolders (arg)](#apidoc.element.dropbox.routes.sharingListMountableFolders)
- description and source-code
```javascript
sharingListMountableFolders = function (arg) {
  return this.request('sharing/list_mountable_folders', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListMountableFoldersContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListMountableFoldersContinue (arg)](#apidoc.element.dropbox.routes.sharingListMountableFoldersContinue)
- description and source-code
```javascript
sharingListMountableFoldersContinue = function (arg) {
  return this.request('sharing/list_mountable_folders/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListReceivedFiles"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListReceivedFiles (arg)](#apidoc.element.dropbox.routes.sharingListReceivedFiles)
- description and source-code
```javascript
sharingListReceivedFiles = function (arg) {
  return this.request('sharing/list_received_files', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListReceivedFilesContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListReceivedFilesContinue (arg)](#apidoc.element.dropbox.routes.sharingListReceivedFilesContinue)
- description and source-code
```javascript
sharingListReceivedFilesContinue = function (arg) {
  return this.request('sharing/list_received_files/continue', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingListSharedLinks"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingListSharedLinks (arg)](#apidoc.element.dropbox.routes.sharingListSharedLinks)
- description and source-code
```javascript
sharingListSharedLinks = function (arg) {
  return this.request('sharing/list_shared_links', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingModifySharedLinkSettings"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingModifySharedLinkSettings (arg)](#apidoc.element.dropbox.routes.sharingModifySharedLinkSettings)
- description and source-code
```javascript
sharingModifySharedLinkSettings = function (arg) {
  return this.request('sharing/modify_shared_link_settings', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingMountFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingMountFolder (arg)](#apidoc.element.dropbox.routes.sharingMountFolder)
- description and source-code
```javascript
sharingMountFolder = function (arg) {
  return this.request('sharing/mount_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRelinquishFileMembership"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRelinquishFileMembership (arg)](#apidoc.element.dropbox.routes.sharingRelinquishFileMembership)
- description and source-code
```javascript
sharingRelinquishFileMembership = function (arg) {
  return this.request('sharing/relinquish_file_membership', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRelinquishFolderMembership"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRelinquishFolderMembership (arg)](#apidoc.element.dropbox.routes.sharingRelinquishFolderMembership)
- description and source-code
```javascript
sharingRelinquishFolderMembership = function (arg) {
  return this.request('sharing/relinquish_folder_membership', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRemoveFileMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFileMember (arg)](#apidoc.element.dropbox.routes.sharingRemoveFileMember)
- description and source-code
```javascript
sharingRemoveFileMember = function (arg) {
  return this.request('sharing/remove_file_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRemoveFileMember2"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFileMember2 (arg)](#apidoc.element.dropbox.routes.sharingRemoveFileMember2)
- description and source-code
```javascript
sharingRemoveFileMember2 = function (arg) {
  return this.request('sharing/remove_file_member_2', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRemoveFolderMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRemoveFolderMember (arg)](#apidoc.element.dropbox.routes.sharingRemoveFolderMember)
- description and source-code
```javascript
sharingRemoveFolderMember = function (arg) {
  return this.request('sharing/remove_folder_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingRevokeSharedLink"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingRevokeSharedLink (arg)](#apidoc.element.dropbox.routes.sharingRevokeSharedLink)
- description and source-code
```javascript
sharingRevokeSharedLink = function (arg) {
  return this.request('sharing/revoke_shared_link', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingShareFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingShareFolder (arg)](#apidoc.element.dropbox.routes.sharingShareFolder)
- description and source-code
```javascript
sharingShareFolder = function (arg) {
  return this.request('sharing/share_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingTransferFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingTransferFolder (arg)](#apidoc.element.dropbox.routes.sharingTransferFolder)
- description and source-code
```javascript
sharingTransferFolder = function (arg) {
  return this.request('sharing/transfer_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUnmountFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnmountFolder (arg)](#apidoc.element.dropbox.routes.sharingUnmountFolder)
- description and source-code
```javascript
sharingUnmountFolder = function (arg) {
  return this.request('sharing/unmount_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUnshareFile"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnshareFile (arg)](#apidoc.element.dropbox.routes.sharingUnshareFile)
- description and source-code
```javascript
sharingUnshareFile = function (arg) {
  return this.request('sharing/unshare_file', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUnshareFolder"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUnshareFolder (arg)](#apidoc.element.dropbox.routes.sharingUnshareFolder)
- description and source-code
```javascript
sharingUnshareFolder = function (arg) {
  return this.request('sharing/unshare_folder', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUpdateFileMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFileMember (arg)](#apidoc.element.dropbox.routes.sharingUpdateFileMember)
- description and source-code
```javascript
sharingUpdateFileMember = function (arg) {
  return this.request('sharing/update_file_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUpdateFolderMember"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFolderMember (arg)](#apidoc.element.dropbox.routes.sharingUpdateFolderMember)
- description and source-code
```javascript
sharingUpdateFolderMember = function (arg) {
  return this.request('sharing/update_folder_member', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.sharingUpdateFolderPolicy"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>sharingUpdateFolderPolicy (arg)](#apidoc.element.dropbox.routes.sharingUpdateFolderPolicy)
- description and source-code
```javascript
sharingUpdateFolderPolicy = function (arg) {
  return this.request('sharing/update_folder_policy', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.usersGetAccount"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetAccount (arg)](#apidoc.element.dropbox.routes.usersGetAccount)
- description and source-code
```javascript
usersGetAccount = function (arg) {
  return this.request('users/get_account', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.usersGetAccountBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetAccountBatch (arg)](#apidoc.element.dropbox.routes.usersGetAccountBatch)
- description and source-code
```javascript
usersGetAccountBatch = function (arg) {
  return this.request('users/get_account_batch', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.usersGetCurrentAccount"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetCurrentAccount (arg)](#apidoc.element.dropbox.routes.usersGetCurrentAccount)
- description and source-code
```javascript
usersGetCurrentAccount = function (arg) {
  return this.request('users/get_current_account', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes.usersGetSpaceUsage"></a>[function <span class="apidocSignatureSpan">dropbox.routes.</span>usersGetSpaceUsage (arg)](#apidoc.element.dropbox.routes.usersGetSpaceUsage)
- description and source-code
```javascript
usersGetSpaceUsage = function (arg) {
  return this.request('users/get_space_usage', arg, 'user', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dropbox.routes_team"></a>[module dropbox.routes_team](#apidoc.module.dropbox.routes_team)

#### <a name="apidoc.element.dropbox.routes_team.teamDevicesListMemberDevices"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListMemberDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListMemberDevices)
- description and source-code
```javascript
teamDevicesListMemberDevices = function (arg) {
  return this.request('team/devices/list_member_devices', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamDevicesListMembersDevices"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListMembersDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListMembersDevices)
- description and source-code
```javascript
teamDevicesListMembersDevices = function (arg) {
  return this.request('team/devices/list_members_devices', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamDevicesListTeamDevices"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesListTeamDevices (arg)](#apidoc.element.dropbox.routes_team.teamDevicesListTeamDevices)
- description and source-code
```javascript
teamDevicesListTeamDevices = function (arg) {
  return this.request('team/devices/list_team_devices', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSession"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesRevokeDeviceSession (arg)](#apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSession)
- description and source-code
```javascript
teamDevicesRevokeDeviceSession = function (arg) {
  return this.request('team/devices/revoke_device_session', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSessionBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamDevicesRevokeDeviceSessionBatch (arg)](#apidoc.element.dropbox.routes_team.teamDevicesRevokeDeviceSessionBatch)
- description and source-code
```javascript
teamDevicesRevokeDeviceSessionBatch = function (arg) {
  return this.request('team/devices/revoke_device_session_batch', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGetInfo"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamGetInfo)
- description and source-code
```javascript
teamGetInfo = function (arg) {
  return this.request('team/get_info', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsCreate"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsCreate (arg)](#apidoc.element.dropbox.routes_team.teamGroupsCreate)
- description and source-code
```javascript
teamGroupsCreate = function (arg) {
  return this.request('team/groups/create', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsDelete"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsDelete (arg)](#apidoc.element.dropbox.routes_team.teamGroupsDelete)
- description and source-code
```javascript
teamGroupsDelete = function (arg) {
  return this.request('team/groups/delete', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsGetInfo"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamGroupsGetInfo)
- description and source-code
```javascript
teamGroupsGetInfo = function (arg) {
  return this.request('team/groups/get_info', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsJobStatusGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamGroupsJobStatusGet)
- description and source-code
```javascript
teamGroupsJobStatusGet = function (arg) {
  return this.request('team/groups/job_status/get', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsList"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsList (arg)](#apidoc.element.dropbox.routes_team.teamGroupsList)
- description and source-code
```javascript
teamGroupsList = function (arg) {
  return this.request('team/groups/list', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsListContinue (arg)](#apidoc.element.dropbox.routes_team.teamGroupsListContinue)
- description and source-code
```javascript
teamGroupsListContinue = function (arg) {
  return this.request('team/groups/list/continue', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsMembersAdd"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersAdd (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersAdd)
- description and source-code
```javascript
teamGroupsMembersAdd = function (arg) {
  return this.request('team/groups/members/add', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsMembersList"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersList (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersList)
- description and source-code
```javascript
teamGroupsMembersList = function (arg) {
  return this.request('team/groups/members/list', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsMembersListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersListContinue (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersListContinue)
- description and source-code
```javascript
teamGroupsMembersListContinue = function (arg) {
  return this.request('team/groups/members/list/continue', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsMembersRemove"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersRemove (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersRemove)
- description and source-code
```javascript
teamGroupsMembersRemove = function (arg) {
  return this.request('team/groups/members/remove', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsMembersSetAccessType"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsMembersSetAccessType (arg)](#apidoc.element.dropbox.routes_team.teamGroupsMembersSetAccessType)
- description and source-code
```javascript
teamGroupsMembersSetAccessType = function (arg) {
  return this.request('team/groups/members/set_access_type', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamGroupsUpdate"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamGroupsUpdate (arg)](#apidoc.element.dropbox.routes_team.teamGroupsUpdate)
- description and source-code
```javascript
teamGroupsUpdate = function (arg) {
  return this.request('team/groups/update', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamLinkedAppsListMemberLinkedApps"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListMemberLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListMemberLinkedApps)
- description and source-code
```javascript
teamLinkedAppsListMemberLinkedApps = function (arg) {
  return this.request('team/linked_apps/list_member_linked_apps', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamLinkedAppsListMembersLinkedApps"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListMembersLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListMembersLinkedApps)
- description and source-code
```javascript
teamLinkedAppsListMembersLinkedApps = function (arg) {
  return this.request('team/linked_apps/list_members_linked_apps', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamLinkedAppsListTeamLinkedApps"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsListTeamLinkedApps (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsListTeamLinkedApps)
- description and source-code
```javascript
teamLinkedAppsListTeamLinkedApps = function (arg) {
  return this.request('team/linked_apps/list_team_linked_apps', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedApp"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsRevokeLinkedApp (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedApp)
- description and source-code
```javascript
teamLinkedAppsRevokeLinkedApp = function (arg) {
  return this.request('team/linked_apps/revoke_linked_app', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedAppBatch"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamLinkedAppsRevokeLinkedAppBatch (arg)](#apidoc.element.dropbox.routes_team.teamLinkedAppsRevokeLinkedAppBatch)
- description and source-code
```javascript
teamLinkedAppsRevokeLinkedAppBatch = function (arg) {
  return this.request('team/linked_apps/revoke_linked_app_batch', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersAdd"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersAdd (arg)](#apidoc.element.dropbox.routes_team.teamMembersAdd)
- description and source-code
```javascript
teamMembersAdd = function (arg) {
  return this.request('team/members/add', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersAddJobStatusGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersAddJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamMembersAddJobStatusGet)
- description and source-code
```javascript
teamMembersAddJobStatusGet = function (arg) {
  return this.request('team/members/add/job_status/get', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersGetInfo"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamMembersGetInfo)
- description and source-code
```javascript
teamMembersGetInfo = function (arg) {
  return this.request('team/members/get_info', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersList"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersList (arg)](#apidoc.element.dropbox.routes_team.teamMembersList)
- description and source-code
```javascript
teamMembersList = function (arg) {
  return this.request('team/members/list', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersListContinue"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersListContinue (arg)](#apidoc.element.dropbox.routes_team.teamMembersListContinue)
- description and source-code
```javascript
teamMembersListContinue = function (arg) {
  return this.request('team/members/list/continue', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersRecover"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRecover (arg)](#apidoc.element.dropbox.routes_team.teamMembersRecover)
- description and source-code
```javascript
teamMembersRecover = function (arg) {
  return this.request('team/members/recover', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersRemove"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRemove (arg)](#apidoc.element.dropbox.routes_team.teamMembersRemove)
- description and source-code
```javascript
teamMembersRemove = function (arg) {
  return this.request('team/members/remove', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersRemoveJobStatusGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersRemoveJobStatusGet (arg)](#apidoc.element.dropbox.routes_team.teamMembersRemoveJobStatusGet)
- description and source-code
```javascript
teamMembersRemoveJobStatusGet = function (arg) {
  return this.request('team/members/remove/job_status/get', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersSendWelcomeEmail"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSendWelcomeEmail (arg)](#apidoc.element.dropbox.routes_team.teamMembersSendWelcomeEmail)
- description and source-code
```javascript
teamMembersSendWelcomeEmail = function (arg) {
  return this.request('team/members/send_welcome_email', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersSetAdminPermissions"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSetAdminPermissions (arg)](#apidoc.element.dropbox.routes_team.teamMembersSetAdminPermissions)
- description and source-code
```javascript
teamMembersSetAdminPermissions = function (arg) {
  return this.request('team/members/set_admin_permissions', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersSetProfile"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSetProfile (arg)](#apidoc.element.dropbox.routes_team.teamMembersSetProfile)
- description and source-code
```javascript
teamMembersSetProfile = function (arg) {
  return this.request('team/members/set_profile', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersSuspend"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersSuspend (arg)](#apidoc.element.dropbox.routes_team.teamMembersSuspend)
- description and source-code
```javascript
teamMembersSuspend = function (arg) {
  return this.request('team/members/suspend', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamMembersUnsuspend"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamMembersUnsuspend (arg)](#apidoc.element.dropbox.routes_team.teamMembersUnsuspend)
- description and source-code
```javascript
teamMembersUnsuspend = function (arg) {
  return this.request('team/members/unsuspend', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamPropertiesTemplateAdd"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateAdd (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateAdd)
- description and source-code
```javascript
teamPropertiesTemplateAdd = function (arg) {
  return this.request('team/properties/template/add', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamPropertiesTemplateGet"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateGet (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateGet)
- description and source-code
```javascript
teamPropertiesTemplateGet = function (arg) {
  return this.request('team/properties/template/get', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamPropertiesTemplateList"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateList (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateList)
- description and source-code
```javascript
teamPropertiesTemplateList = function (arg) {
  return this.request('team/properties/template/list', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamPropertiesTemplateUpdate"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamPropertiesTemplateUpdate (arg)](#apidoc.element.dropbox.routes_team.teamPropertiesTemplateUpdate)
- description and source-code
```javascript
teamPropertiesTemplateUpdate = function (arg) {
  return this.request('team/properties/template/update', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamReportsGetActivity"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetActivity (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetActivity)
- description and source-code
```javascript
teamReportsGetActivity = function (arg) {
  return this.request('team/reports/get_activity', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamReportsGetDevices"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetDevices (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetDevices)
- description and source-code
```javascript
teamReportsGetDevices = function (arg) {
  return this.request('team/reports/get_devices', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamReportsGetMembership"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetMembership (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetMembership)
- description and source-code
```javascript
teamReportsGetMembership = function (arg) {
  return this.request('team/reports/get_membership', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamReportsGetStorage"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamReportsGetStorage (arg)](#apidoc.element.dropbox.routes_team.teamReportsGetStorage)
- description and source-code
```javascript
teamReportsGetStorage = function (arg) {
  return this.request('team/reports/get_storage', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderActivate"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderActivate (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderActivate)
- description and source-code
```javascript
teamTeamFolderActivate = function (arg) {
  return this.request('team/team_folder/activate', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderArchive"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderArchive (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderArchive)
- description and source-code
```javascript
teamTeamFolderArchive = function (arg) {
  return this.request('team/team_folder/archive', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderArchiveCheck"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderArchiveCheck (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderArchiveCheck)
- description and source-code
```javascript
teamTeamFolderArchiveCheck = function (arg) {
  return this.request('team/team_folder/archive/check', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderCreate"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderCreate (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderCreate)
- description and source-code
```javascript
teamTeamFolderCreate = function (arg) {
  return this.request('team/team_folder/create', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderGetInfo"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderGetInfo (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderGetInfo)
- description and source-code
```javascript
teamTeamFolderGetInfo = function (arg) {
  return this.request('team/team_folder/get_info', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderList"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderList (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderList)
- description and source-code
```javascript
teamTeamFolderList = function (arg) {
  return this.request('team/team_folder/list', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderPermanentlyDelete"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderPermanentlyDelete (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderPermanentlyDelete)
- description and source-code
```javascript
teamTeamFolderPermanentlyDelete = function (arg) {
  return this.request('team/team_folder/permanently_delete', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dropbox.routes_team.teamTeamFolderRename"></a>[function <span class="apidocSignatureSpan">dropbox.routes_team.</span>teamTeamFolderRename (arg)](#apidoc.element.dropbox.routes_team.teamTeamFolderRename)
- description and source-code
```javascript
teamTeamFolderRename = function (arg) {
  return this.request('team/team_folder/rename', arg, 'team', 'api', 'rpc');
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
