## 행정동코드 json 작성하기(만들기)
### PublicDataReader 참고
- https://github.com/WooilJeong/PublicDataReader/blob/main/etc/create_code_bdong_file.ipynb

## 데이터프레임을 딕셔너리로 변환
bdong_dict = 법정동코드.to_dict()
hdong_dict = 행정동코드.to_dict()

with open('/'.join([xls_path,"code_bdong.json"]) , "w") as f:
    f.write(json.dumps(bdong_dict))
    f.close()

with open('/'.join([xls_path,"code_hdong.json"]) , "w") as f:
    f.write(json.dumps(hdong_dict))
    f.close()

## 다운로드 출처
- https://www.mois.go.kr/frt/bbs/type001/commonSelectBoardList.do?bbsId=BBSMSTR_000000000052
