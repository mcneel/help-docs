---
title: 옵션 Flamingo nXt
---


# ![images/options.svg](images/options.svg) {{page.title}}
These settings apply to the Flamingo application.  Making changes here change how Flamingo runs all the time.

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### 팜 공유 폴더
{: #farm-output-folder}
The shared folder for render farm jobs. This is also the location that the farm will output its results. Use the Folder icon ![images/folderopen32x32.png](images/folderopen32x32.png) to select a new location.

#### 태그된 조명 표시
이 속성을 사용하여 태그된 조명의 방향을 표시합니다. 집중 및 확산 배광에서 실행됩니다.

#### OpenGL에서 빠른 미리보기
This changes the material thumbnails to start with an OpenGL thumbnail before the rendered material is returned.  This can lead to faster responses on material, but the OpenGL image may not be close to the actual material.

#### 렌더링이 완료되면 네이티브 히스토리 파일 저장
By default Flamingo will cache the last image rendered in case there is a need to return to it in the future.
