---
---


# Options: Flamingo nXt

## Library folders
{: #library-folders}
사용 가능한 재질과 식물 라이브러리 목록을 만들 때 스캔할 추가적인 폴더 위치. 기본적으로 이 목록은 비어 있습니다.

## File search paths
{: #file-search-paths}
The folders are not searched for libraries, but rather for support files, such as bitmaps, plant textures, in addition to the **Library folders**. The folders are searched in order they appear in the list. The current folder containing the .3DM file is searched first.

#### 새 폴더 추가
1.
Under **Library folders**, click the **New** icon.
2.
In the **Browse for Folder** dialog box, select a folder.

#### Delete a folder

>Select a folder name from the list, and click the Delete icon.

#### To move a folder up in the list

>Select a folder name from the list, and click the Move Up icon.

#### To move a folder down in the list

>Select a folder name from the list, and click the Move Down icon.

### Allow modeling while rendering
{: #modal-rendering}
렌더링이 실행되는 동안에도 계속해서 모델링 작업을 할 수 있습니다.

### Insert plants as point clouds
{: #insert-plants-as-point-clouds}
식물을 나타내기 위해 점구름을 사용합니다. 점구름을 사용하면 일반적으로 파일 크기가 더욱 작아집니다.
점구름을 사용하지 않는 경우, 식물은 메쉬 개체로 표시됩니다.
*![images/treespointcloudormesh.png](images/treespointcloudormesh.png)Trees as point cloud (left) and mesh (right).*

## Default image link state
{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}
### Decal drag transparency
{: #drag-transparency}
{: #decal-editing}
데칼을 배치하기 위해 마우스로 끌어오는 동안 표시되는 투명도를 지정합니다.

### Default material preview size
{: #default-material-preview-size}
Specifies the default size of the material preview sphere in the [Material Editor](advanced-material-properties-main.html#preview).

### Farm output folder
{: #farm-output-folder}
렌더 팜 작업이 출력되는 폴더입니다.
