DREAMFOREN 시료채취기록 웹 v94

기준: v89 안정본
핵심 변경:
1. Supabase companies/facilities를 업체·시설 단일 원본으로 사용
2. Supabase companies가 비어 있어도 embedded/local DB 자동 업로드 금지
3. facilities의 facility_name을 우선 사용하고, 사각 치수는 정규화 컬럼 fallback 지원
4. 업체/시설 저장 시 Supabase에 반영하며 시설 삭제도 해당 업체 범위에서 동기화
5. 계약 신규/수정 저장 시 해당 업체가 companies에 없으면 사업자번호 우선으로 업체 마스터 자동 생성
6. 계약 저장 후 companies/facilities를 다시 pull하여 업체관리/시료채취 선택기에 즉시 반영

주의:
- Supabase 기반정비 완료(companies 345 / facilities 1094 / contracts 473) 상태를 전제로 합니다.
- 신규 계약의 신규 업체는 업체 마스터가 생성되지만 시설은 자동 생성하지 않습니다. 업체관리에서 실제 시설정보를 등록해야 합니다.
- 기존 embedded DB는 file:// 비상 표시용으로 코드에 남아 있으나 온라인 DB를 자동 덮어쓰지 않습니다.
