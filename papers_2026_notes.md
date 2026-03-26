# papers_2026_notes

## 1. Parabrachial CGRP Neurons Regulate Opioid Reinforcement

### 핵심 질문
PBN의 CGRP 뉴런이 단순히 aversion/pain 관련 세포가 아니라, opioid reinforcement에도 직접 관여하는가?

### 왜 중요한가
기존에는 PBN CGRP 뉴런이 주로 aversive state, malaise, pain relay 쪽으로 알려져 있었다. 이 논문은 이 세포군이 opioid abstinence와 drug-taking behavior 모두에 걸쳐 기능적 역할을 할 수 있음을 제시한다.

### Methods
- Calca-Cre 마우스 사용
- 바이러스 기반 nuclear labeling
- FANS로 CGRP^PBN 핵 분리
- 핵 RNA-seq 수행
- chronic morphine exposure 및 abstinence 유도
- cFos immunostaining으로 세포 활성 측정
- morphine IV self-administration
- hM4Di DREADD 기반 chemogenetic inhibition

### Figure-by-figure
#### Figure 1
CGRP^PBN 뉴런을 분리하고 전사체를 정의한다. 이 단계의 목적은 이후 조작할 세포군의 molecular identity를 먼저 명확히 하는 것이다.

#### Figure 2
CGRP^PBN-enriched genes를 보여준다. neuropeptide 관련 유전자와 opioid-related genes가 enrichment되어 있어 이 세포군이 opioid state에 반응할 분자적 기반을 가진다는 점을 제시한다.

#### Figure 3
Morphine abstinence 초기에 CGRP^PBN 뉴런의 cFos가 증가하고 이후 감소한다. 즉 이 세포군은 drug presence보다 abstinence state에 더 민감하다.

#### Figure 4
CGRP^PBN 억제가 morphine intake를 감소시킨다. 이 결과는 이 세포군이 실제 reinforcement에 기능적으로 기여함을 보여준다.

#### Figure 5
Dose-response와 seeking 관련 분석. 낮은 morphine dose에서 intake 감소 효과가 뚜렷하고, 후기 seeking/reinstatement는 크게 바뀌지 않는다. 즉 reinforcement 쪽 역할이 더 강하다.

### 한줄 정리
CGRP^PBN 뉴런은 opioid abstinence에 반응하고, morphine reinforcement를 조절하는 기능적 세포군이다.

---

## 2. Cardiac signals shape insular cortex activity and emotion coding

### 핵심 질문
Posterior insular cortex가 심장 신호를 어떻게 코딩하며, 그 cardiac coding이 emotion representation에 실제로 필요한가?

### 왜 중요한가
Insula는 interoceptive cortex로 알려져 있었지만, heartbeat-level precision으로 심장 신호를 다루는지, 그리고 그것이 emotion coding에 어떤 인과적 역할을 하는지는 불명확했다.

### Methods
- Head-fixed mouse preparation
- Whole-cell patch clamp recording
- Silicon probe single-unit recording
- ECG, pupil, locomotion 동시 측정
- Appetitive/aversive cue paradigm
- β-adrenergic blocker metoprolol 투여
- Decoding analysis로 cue identity와 emotional state 구분 능력 평가

### Figure-by-figure
#### Figure 1
pInsCtx membrane potential이 heart rate changes 및 cardiac cycle과 coupling됨을 보여준다.

#### Figure 2
Single-neuron 수준에서 heartbeat tuning을 보여준다. 많은 뉴런이 특정 heartbeat frequency band에 선택적으로 tuned된다.

#### Figure 3
Appetitive 및 aversive state에서 heartbeat tuning이 더 강해진다. emotion context가 cardioceptive gain을 높인다는 뜻이다.

#### Figure 4
Metoprolol로 sympathetic cardiac arousal을 줄이면 heartbeat tuning과 heart-rate sensing이 약해지고, insula activity로부터 cue identity를 decode하는 능력도 무너진다.

### Metoprolol의 의미
이 논문에서 metoprolol은 심장 기반 감정 각성 신호를 약화시키는 도구다. 즉 감정 cue가 유발하는 bodily arousal 중 cardiac component를 줄여서, insula의 emotion coding이 cardiac input에 얼마나 의존하는지 테스트한다.

### 한줄 정리
Insula는 심장 신호를 정밀하게 코딩하며, 이 cardiac interoceptive input은 emotion representation의 핵심 재료다.

---

## 3. Statistics of natural scenes shape contextual modulation in the visual cortex

### 핵심 질문
V1 surround modulation은 왜 생기며, 자연 장면에서 주변 문맥은 center stimulus 반응을 어떤 원리로 조절하는가?

### 왜 CNN을 쓰는가
이 논문에서 CNN은 ‘이미지 분류용 AI’로 쓰인 것이 아니라, 각 V1 뉴런이 이미지에 어떻게 반응하는지 예측하는 **neural response model**로 쓰였다. 즉 입력은 이미지, 출력은 실제 recorded neuron response이다. 학습이 끝나면 이 모델은 새로운 이미지가 들어왔을 때 해당 뉴런이 얼마나 반응할지 예측할 수 있다.

### CNN을 neuron data로 어떻게 만드는가
- 실제 실험에서 다양한 natural image를 제시
- 각 이미지에 대한 실제 V1 neuron response를 측정
- CNN이 이미지에서 feature를 추출하고 각 neuron의 response를 예측하도록 학습
- loss를 줄이도록 파라미터를 업데이트
- 결과적으로 ‘이 뉴런의 digital twin’처럼 작동하는 예측 모델이 됨

### 이 모델을 왜 필요로 하나
이 모델이 있으면 역으로 optimization을 해서
- 어떤 center image가 neuron을 가장 잘 흥분시키는지(MEI)
- 어떤 surround가 center response를 증가시키는지
- 어떤 surround가 response를 감소시키는지
를 찾을 수 있다.

### 아주 쉬운 핵심 개념
- 주변 문맥이 center 패턴을 자연스럽게 이어주면 반응이 유지되거나 증가함
- 주변 문맥이 center 패턴을 부자연스럽게 깨면 반응이 감소함

### Methods
- Awake mouse V1 recording
- Natural image response dataset 수집
- CNN-based digital twin training
- MEI optimization
- Facilitatory/suppressive surround optimization
- Closed-loop in vivo validation
- Diffusion-model outpainting 비교
- Macaque predictive model 일반화
- Bayesian generative model

### Figure-by-figure
#### Figure 1
CNN digital twin이 neuron responses를 잘 예측할 수 있음을 보여준다.

#### Figure 2
각 neuron의 MEI와 facilitatory/suppressive surround를 optimization으로 찾고, 실제 실험에서 그 효과를 검증한다.

#### Figure 3
Facilitatory surround는 center 패턴을 자연스럽게 이어주는 형태이고, suppressive surround는 그 continuation을 깨는 형태임을 보여준다.

#### Figure 4
이 원리가 다양한 neuron과 조건에서 재현됨을 보여준다.

#### Figure 5
Mouse에서 본 원리가 macaque에서도 유사하게 나타남을 보여준다.

#### Figure 6
Hierarchical Bayesian model로 surround modulation을 설명한다. 즉 뇌는 center를 고립된 조각으로 보지 않고 전체 scene의 일부로 추론한다.

### 한줄 정리
V1은 가운데 자극만 따로 보는 것이 아니라, 주변 문맥이 그 자극을 자연스럽게 완성하는지 여부에 따라 반응을 바꾼다.

---

## 4. Parasites trigger epithelial cell crosstalk to drive gut-brain signalling

### 핵심 질문
Parasite sensing이 장 상피세포를 통해 어떻게 신경계 신호로 바뀌고, feeding suppression 같은 방어 행동을 유도하는가?

### 왜 중요한가
Immune sensing과 gut-brain signaling을 separate system으로 볼 것이 아니라, epithelial cell-level relay를 통해 하나의 defense axis로 볼 수 있음을 보여준다.

### 등장인물
- Tuft cell: parasite/metabolite sensing, ACh source
- EC cell (enterochromaffin cell): serotonin source, sensory nerve activation

### 핵심 메커니즘
1. Tuft cell이 ACh를 분비
2. ACh가 crypt EC cell의 muscarinic receptor를 자극
3. EC cell이 serotonin 분비
4. Serotonin이 vagal afferent를 자극
5. Brainstem을 거쳐 feeding suppression 유도

### Methods
- Organoid system
- EC cell calcium imaging
- Serotonin biosensor cell assay
- Receptor expression analysis
- Pharmacology (atropine, mecamylamine)
- Parasite-derived metabolite stimulation
- Vagal afferent readout
- Feeding behavior assay

### Figure-by-figure
#### Figure 1
ACh가 crypt EC cell calcium response와 serotonin release를 유도하며, 이 반응이 muscarinic signaling에 의존함을 보여준다.

#### Figure 2
Tuft cell이 parasite-derived metabolite에 반응해 acute ACh release를 할 수 있음을 보여준다.

#### Figure 3
Type 2 inflammation이 형성되면 tuft cell ACh release가 더 지속적이고 leak-like한 형태를 띠게 됨을 제시한다.

#### Figure 4
Sustained ACh signaling만이 충분한 EC serotonin release를 유도해 vagal afferent activation threshold를 넘길 수 있음을 보여준다.

#### Figure 5
이 epithelial relay가 실제로 feeding suppression 같은 protective behavior를 유도함을 보여준다.

#### Figure 6
초기 감염과 진행된 감염 단계의 차이를 설명하는 모델. 초기에는 signal이 약해 행동 변화가 작고, type 2 inflammation 이후에는 tuft→EC→vagus signal이 커져 행동 효과가 나타난다.

### 비전공자용 한줄 정리
기생충 감염이 장 상피세포들 사이의 ACh→serotonin relay를 통해 뇌로 전달되고, 그 결과 먹는 행동이 줄어든다.

---

## 5. Epigenetic memory of colitis promotes tumour growth

### 핵심 질문
만성 대장염이 끝난 뒤에도 장 줄기세포가 염증을 기억하고 있으며, 그 기억이 미래의 종양 성장을 촉진하는가?

### 왜 중요한가
염증이 암 위험을 높인다는 것은 알려져 있었지만, 이 논문은 mutation 증가만이 아니라 stem cell의 long-lived epigenetic memory가 중요한 연결고리일 수 있음을 보여준다.

### Epigenetic memory란
DNA sequence가 바뀌는 것이 아니라, 특정 유전자 조절 영역이 더 열려 있고 TF가 더 잘 붙는 상태가 오래 남는 것이다. 이 논문에서는 특히 AP-1 accessibility가 오래 유지된다.

### SHARE-TRACE란 무엇인가
SHARE-TRACE는 single-cell 수준에서 동시에
- RNA expression
- chromatin accessibility
- clonal history
를 함께 추적하는 방법이다.

이 기술 덕분에 저자들은 colitis memory가 단순히 주변 환경 때문이 아니라, 같은 clone 계열 안에서 이어지는 **cell-intrinsic, clonally inherited memory state**라는 점을 보여줄 수 있었다.

### Methods
- DSS chronic colitis model
- Acute, chronic, recovered time points 비교
- Single-cell chromatin accessibility + gene expression 분석
- SHARE-TRACE
- Organoid clone analysis
- Apc-loss tumour initiation model
- AP-1 inhibitor T-5224 treatment

### Figure-by-figure
#### Figure 1
Recovery 후에도 stem/progenitor population에서 AP-1 accessibility가 높게 남아 있음을 보여준다. RNA는 대부분 회복되지만 chromatin memory는 지속된다.

#### Figure 2
Colitis-derived clone들이 높은 AP-1 accessibility를 유지하고, clone마다 memory 강도가 다름을 보여준다. 즉 memory는 clonal하고 cell-intrinsic하다.

#### Figure 3
AP-1 memory state가 FOX family TF cooperation 등과 함께 유지될 수 있음을 보여준다.

#### Figure 4
Recovered mice에서 Apc loss로 tumour를 유도하면 더 큰 종양이 생기며, AP-1 inhibitor는 이 효과를 크게 줄인다. 즉 colitis memory가 tumour outgrowth를 실제로 촉진한다.

### 비전공자용 아주 쉬운 설명
대장염이 끝난 뒤에도 줄기세포는 ‘상처 복구 모드’를 기억하고 있다. 나중에 암 돌연변이가 생기면 이 기억 때문에 종양이 더 빨리 자란다.

### 한줄 정리
만성 대장염은 줄기세포에 AP-1 중심 epigenetic memory를 남기고, 이 기억이 미래 tumour outgrowth를 가속한다.

---

## GitHub 업로드용 간단 가이드

### 방법 1. 웹에서 직접 업로드
1. GitHub 저장소 `papers_interesting` 열기
2. `Add file` 클릭
3. `Create new file` 선택
4. 파일 이름에 `papers_2026_notes.md` 입력
5. 이 문서 내용을 전체 복사해서 붙여넣기
6. 아래쪽 `Commit new file` 클릭

### 방법 2. 로컬에서 git 사용
```bash
git clone https://github.com/limserenahansol/papers_interesting.git
cd papers_interesting
# papers_2026_notes.md 파일 저장
 git add papers_2026_notes.md
 git commit -m "Add 2026 paper notes"
 git push origin main
```

### 추천
지금은 웹에서 직접 업로드하는 방법이 가장 간단하다.

