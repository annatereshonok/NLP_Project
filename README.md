# VK groups clustering (and followers analysis)

The main goal of the project is to characterize VK communities through the text cluster analysis and to identify if the group toipics clustering is consistent with the participants based clustering.

In order to achieve the goal we:
- declared VK parser functions
- performed text normalization and text tokenisation
- conducted different clustering using (TF-IDF based k-means clustering, DBSCAN clustering)
- conducted clustering using Jaccard similarity based on the followers number amd intercept

The data was retrieved from VK.com using VK API. 
These are the methods used for data pursuit
- groups.search (https://vk.com/dev/groups.search) - enables you to get the results of group search using some query
- wall.get (https://vk.com/dev/wall.get) enables you to get posts of a community or a person
- groups.getMembers (https://vk.com/dev/groups.getMembers) is used to get members ids. However, you cannot get more than 1000 followers ids

The data are the Russian texts of 100 posts per the community (posts are joined in one text per group). The groups were taken using 3 search queries: music, science, books. We have taken the first 300 groups per category (default vk sorting).

As a result, we found out that clustering algorithms used produce different results, but are able to distinguish different topic. For the future development we are going to parse data on group followers ids, perform Jaccard measure based clustering and identify if users follow the same interest patterns.
