import ipywidgets as widgets
from IPython.display import display
import seaborn as sns

data_dropdown = widgets.Dropdown(
    options=[
        ("anagrams: 단어 전환 작업 반응 시간", "anagrams"),
        ("anscombe: 통계값 같지만 분포 다른 4분할", "anscombe"),
        ("attention: 시각 주의 실험 반응 시간", "attention"),
        ("brain_networks: 뇌 연결망 데이터", "brain_networks"),
        ("car_crashes: 주별 차량 사고 통계", "car_crashes"),
        ("diamonds: 다이아몬드 가격 분석", "diamonds"),
        ("dots: 시각 자극에 대한 시계열 반응", "dots"),
        ("dowjones: 다우존스 산업지수 월별 변동", "dowjones"),
        ("exercise: 성별·운동별 심박수 반응", "exercise"),
        ("flights: 항공 승객 수 시계열", "flights"),
        ("fmri: 뇌 반응 시간 시계열", "fmri"),
        ("geyser: 간헐천 분출 간격/지속시간", "geyser"),
        ("glue: 점성/접착도 테스트", "glue"),
        ("healthexp: 국가별 보건 지출 vs 기대수명", "healthexp"),
        ("iris: 붓꽃 분류 데이터", "iris"),
        ("mpg: 자동차 연비 및 배기량", "mpg"),
        ("penguins: 펭귄 종 분류 (부리, 섬 등)", "penguins"),
        ("planets: 외계 행성 발견 시기 및 질량", "planets"),
        ("seaice: 북극·남극 해빙 면적 시계열", "seaice"),
        ("taxis: 뉴욕 택시 운행 기록", "taxis"),
        ("tips: 팁 예측 데이터", "tips"),
        ("titanic: 타이타닉 생존자 예측", "titanic"),
    ],
    value='flights',
    description='데이터셋 선택:',
    style={"description_width": "initial"},
    layout=widgets.Layout(width="400px")
)
# 선택 시 출력되는 함수 정의
def show_seaborn_dataset(dataset_name):
    df = sns.load_dataset(dataset_name)
    display(df.head())
# 드롭다운을 함수와 연결
out = widgets.interactive_output(show_seaborn_dataset, {'dataset_name': data_dropdown})
