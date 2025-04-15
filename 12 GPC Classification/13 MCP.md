For the implementation of a classification service we looked at the Model Context Protocol (MCP), which unifies the usage of external tools and resources for LLMs.
![[Pasted image 20250415155519.png]]

What we have done is basicly written a small wrapper around the GPC-Explorer package (for now only the english version : https://gitlab.rlp.net/KE3P/gpc/-/tree/english?ref_type=heads) using the fastmcp package: https://gitlab.rlp.net/KE3P/gpc-classification/gpc-mcp-server. With this we managed to achieve the following exemplary conversations with claude sonnet 3.7 using the free tier of claude desktop: 

![[Screenshot from 2025-04-15 10-32-47.png]]![[Screencast from 2025-04-15 15-45-08.webm]]