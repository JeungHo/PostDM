## 행정동코드 json 작성하기(만들기)
### PublicDataReader 참고
- https://github.com/WooilJeong/PublicDataReader/blob/main/etc/create_code_bdong_file.ipynb

## 데이터프레임을 딕셔너리로 변환
<pre>
bdong_dict = 법정동코드.to_dict()
hdong_dict = 행정동코드.to_dict()

with open('/'.join([xls_path,"code_bdong.json"]) , "w") as f:
    f.write(json.dumps(bdong_dict))
    f.close()

with open('/'.join([xls_path,"code_hdong.json"]) , "w") as f:
    f.write(json.dumps(hdong_dict))
    f.close()
</pre>
## 행정안정부 주민등록,인감
- https://www.mois.go.kr/frt/bbs/type001/commonSelectBoardList.do?bbsId=BBSMSTR_000000000052
- "행정안전부 표준코드"가 아니라는 이유가 있구요. api서비스 요청은 했는데 답볍은 "'27년 상반기 중으로 행정동코드를 API 형식으로 제공"하도록 하겠다고 하네요.
--------------------------------------------------
<pre>
현재 행정안전부 홈페이지에서 개별적으로 확인이 필요한 행정동코드 정보를 공공데이터로 제공하는 방안에 대하여 내부적으로 검토한 바,
2026년 주민등록시스템 기능개선 사업 시, 과업에 포함하는 것으로 결정 하였습니다.
이에 따라, '26년 기능개선 과업이 완료되는 시점인 '27년 상반기 중으로 행정동코드를 API 형식으로 제공 받을 수 있도록 개선 추진하겠습니다
</pre>

