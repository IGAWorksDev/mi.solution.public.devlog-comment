# mi.solution.public.devlog-comment
## 기본설명
[giscus](https://giscus.app/ko)를 활용하여 devlog에 댓글과 반응 남기기 기능을 추가했습니다.

## 적용 코드
- [mi.solution.devlog](https://github.com/IGAWorksDev/mi.solution.devlog/blob/345da43cff7172bfc1996723cf6c3cf111cd52f7/front/pages/%5B...id%5D.tsx#L166) front 에 적용된 코드입니다.
- Giscus 코드를 보게되면 repo 주소가 필요합니다. 여기에 사용하기 위해 만들어진 저장소입니다.
- 열견된 페이지에 댓글이나 반으을 남기게 되면 Git의 [Discussions](https://github.com/IGAWorksDev/mi.solution.public.devlog-comment/discussions) 메뉴에 제목과 함께 Disscussion이 하나 추가됩니다.
- (https://giscus.app/ko 페이지를 통해 repoId, cateogoryId를 확인할 수 있습니다.)
```js
    private renderPostComments = () => {
        try {
            return (<Giscus
                id="comments"
                repo="IGAWorksDev/mi.solution.public.devlog-comment"
                repoId="****"
                category="Comments"
                categoryId="***"
                mapping="og:title"
                reactionsEnabled="1"
                emitMetadata="0"
                inputPosition="top"
                theme="light"
                lang="en"
                loading="lazy"
            />)
        } catch (error) {
            console.log("Giscus error",error);
        }
    }
```
