<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-VYQYCC9ZZS"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-VYQYCC9ZZS');
</script>
# Neo4j 사용해보기
---

## Cypher
Cypher란 neo4j만의 그래프 쿼리 언어이다. 노드와 노드간의 관계를 표현한다. 기본 문법은 다음과 같다.

```
(nodes)-[:CONNECT_TO]→(otherNodes)
```

**()**는 노드를, **[:]**는 relation을 나타낸다. 

## Cypher로 Query하기
cypher를 통한 질의는 훨씬 간편하고 정확하다. 테이블의 join 없이도 cypher를 활용한 질의로 단 두 줄 만에 쿼리할 수 있다.

예르 들어, 영화 matrix에 출연한 배우를 찾는다고 하면

```
MATCH (actor:Actor)-[:ACTED_IN]->(movie:Movie {title: 'The Matrix'})
RETURN actor.name
```

두 쿼리 문으로 찾을 수 있다.

