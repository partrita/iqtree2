IQ-TREE
=======

[![Github IQ-TREE 1 Releases](https://img.shields.io/github/downloads/Cibiv/IQ-TREE/total.svg?style=social&logo=github&label=iqtree1%20download)](https://github.com/Cibiv/IQ-TREE/releases)
[![Github IQ-TREE 2 Releases](https://img.shields.io/github/downloads/iqtree/iqtree2/total.svg?style=social&logo=github&label=iqtree2%20download)](https://github.com/iqtree/iqtree2/releases)
[![BioConda downloads](https://img.shields.io/conda/dn/bioconda/iqtree.svg?style=flag&label=BioConda%20install)](https://anaconda.org/bioconda/iqtree)
[![BioConda platforms](https://img.shields.io/conda/pn/bioconda/iqtree?style=flag)](https://github.com/bioconda/bioconda-recipes/tree/master/recipes/iqtree)
[![Build Status](https://github.com/iqtree/iqtree2/workflows/Build/badge.svg)](https://github.com/iqtree/iqtree2/actions)
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

최대 가능도에 의한 효율적이고 다양한 기능을 제공하는 계통유전체학 소프트웨어 <http://www.iqtree.org>

소개
------------

IQ-TREE 소프트웨어는 IQPNNI와 [TREE-PUZZLE](http://www.tree-puzzle.de)의 후속으로 만들어졌습니다(따라서 IQ-TREE라는 이름이 붙었습니다). IQ-TREE는 계통유전체학 데이터의 급격한 축적으로 인해 대량의 데이터를 처리하고 더 복잡한 염기 서열 진화 모델을 제공할 수 있는 효율적인 계통유전체학 소프트웨어의 필요성이 대두되면서 개발되었습니다. 이를 위해 IQ-TREE는 멀티코어 컴퓨터와 분산 병렬 컴퓨팅을 활용하여 분석 속도를 높일 수 있습니다. IQ-TREE는 중단된 분석을 재개하기 위해 자동으로 검사점(checkpointing)을 수행합니다.

입력으로 IQ-TREE는 PHYLIP, FASTA, Nexus, Clustal, MSF를 포함한 모든 일반적인 염기 서열 정렬 형식을 허용합니다. 출력으로 IQ-TREE는 자체적으로 읽을 수 있는 보고서 파일(이름 접미사 `.iqtree`), [FigTree](http://tree.bio.ed.ac.uk/software/figtree/), [Dendroscope](http://dendroscope.org) 또는 [iTOL](http://itol.embl.de)과 같은 트리 뷰어 프로그램으로 시각화할 수 있는 NEWICK 트리 파일(`.treefile`)을 작성합니다.


IQ-TREE의 주요 기능
-----------------------

* __효율적인 검색 알고리즘__: 최대 가능도에 의해 계통수를 재구성하는 빠르고 효과적인 확률적 알고리즘입니다. IQ-TREE는 비슷한 계산 시간을 요구하면서도 가능도 측면에서 RAxML 및 PhyML과 비교하여 유리합니다([Nguyen et al., 2015]).
* __초고속 부트스트랩__: 분기 지원을 평가하기 위한 초고속 부트스트랩 근사(UFBoot)입니다. UFBoot는 RAxML 신속 부트스트랩보다 10~40배 빠르며 편향이 적은 지원 값을 얻습니다([Minh et al., 2013]).
* __정확한 모델 선택__: jModelTest 및 ProtTest보다 10~100배 빠른 초고속 자동 모델 선택(ModelFinder)입니다. ModelFinder는 또한 PartitionFinder와 같이 가장 적합한 분할 체계를 찾습니다([Kalyaanamoorthy et al., 2017]).
* __정렬 시뮬레이션__: Seq-Gen 및 INDELible보다 더 현실적인 모델 하에서 염기 서열 정렬을 시뮬레이션할 수 있는 유연한 시뮬레이터(AliSim)입니다([Ly-Trong et al., 2023]).
* __계통 발생학적 테스트__: SH-aLRT 및 aBayes 테스트([Anisimova et al., 2011])와 같은 여러 빠른 분기 테스트와 근사적으로 편향되지 않은(AU) 테스트([Shimodaira, 2002])와 같은 트리 토폴로지 테스트가 있습니다.


IQ-TREE의 강점은 다양한 계통 발생 모델을 사용할 수 있다는 것입니다.

* __일반 모델__: DNA, 단백질, 코돈, 이진 및 형태학적 데이터에 대한 모든 [일반적인 치환 모델](http://www.iqtree.org/doc/Substitution-Models)과 [사이트 간 비율 이질성](http://www.iqtree.org/doc/Substitution-Models#rate-heterogeneity-across-sites) 및 예를 들어 SNP 데이터에 대한 [확인 편향 보정](http://www.iqtree.org/doc/Substitution-Models#ascertainment-bias-correction)을 제공합니다.
* __[분할 모델](http://www.iqtree.org/doc/Complex-Models/#partition-models)__: 서로 다른 게놈 위치(예: 유전자 또는 코돈 위치), 혼합 데이터 유형, 혼합 비율 이질성 유형, 분할 간 연결되거나 연결되지 않은 분기 길이에 대해 개별 모델을 허용합니다.
* __혼합 모델__: [완전 맞춤형 혼합 모델](http://www.iqtree.org/doc/Complex-Models#mixture-models) 및 [경험적 단백질 혼합 모델](http://www.iqtree.org/doc/Substitution-Models#protein-models)을 제공합니다.
* __다형성 인식 모델 (PoMo)__: <http://www.iqtree.org/doc/Polymorphism-Aware-Models>


IQ-TREE 웹 서비스
-------------------

빠른 시작을 위해 전용 컴퓨팅 클러스터를 사용하여 온라인 계산을 수행하는 IQ-TREE 웹 서버를 사용해 볼 수도 있습니다. 단 3번의 클릭만으로 매우 쉽게 사용할 수 있습니다! 다음에서 사용해 보세요.

* 비엔나 생물정보학 클러스터: <http://iqtree.cibiv.univie.ac.at>
* CIPRES 게이트웨이: <https://www.phylo.org>
* 로스앨러모스 국립 연구소: <https://www.hiv.lanl.gov/content/sequence/IQTREE/iqtree.html>

사용자 지원
------------

[사용자 설명서](http://www.iqtree.org/doc/) 및 [자주 묻는 질문](http://www.iqtree.org/doc/Frequently-Asked-Questions)을 참조하십시오. 추가 질문이나 피드백이 있는 경우 [Github 토론](https://github.com/iqtree/iqtree2/discussions)에 주제를 만드십시오. 기능 요청이나 버그 보고는 [Github 문제](https://github.com/iqtree/iqtree2/issues)에 주제를 게시하십시오.

인용
---------

IQ-TREE 2에 대한 일반적인 인용:

* B.Q. Minh, H.A. Schmidt, O. Chernomor, D. Schrempf, M.D. Woodhams, A. von Haeseler, R. Lanfear (2020) 
  IQ-TREE 2: 게놈 시대의 계통 발생 추론을 위한 새로운 모델 및 효율적인 방법.
  *Mol. Biol. Evol.*, 37:1530-1534. <https://doi.org/10.1093/molbev/msaa015>

또한 IQ-TREE의 주목할 만한 기능과 관련된 다른 논문들이 있으며, 일반적으로 해당 설명서에 언급되어 있습니다. IQ-TREE 코드를 지속적으로 유지하기 위한 자금 확보에 중요한 이러한 논문들도 인용해 주시기를 부탁드립니다. 이러한 논문들은 아래에도 나열되어 있습니다.

트리 혼합 모델(MAST)을 사용하는 경우 다음을 인용하십시오.

* T.K.F. Wong, C. Cherryh, A.G. Rodrigo, M.W. Hahn, B.Q. Minh, R. Lanfear (2024)
  MAST: 사이트와 트리에 걸친 혼합을 이용한 계통 발생 추론.
  _Syst. Biol._, 인쇄 중. <https://doi.org/10.1093/sysbio/syae008>

일치 계수(concordance factors)를 계산하는 경우 다음을 인용하십시오.

* Y.K. Mo, R. Lanfear, M.W. Hahn, B.Q. Minh (2023)
  업데이트된 사이트 일치 계수는 동형 형질 및 분류군 샘플링의 영향을 최소화합니다.
  _Bioinformatics_, 39:btac741. <https://doi.org/10.1093/bioinformatics/btac741>

AliSim을 사용하여 정렬을 시뮬레이션하는 경우 다음을 인용하십시오.

* N. Ly-Trong, G.M.J. Barca, B.Q. Minh (2023)
  AliSim-HPC: 계통 발생학을 위한 병렬 염기 서열 시뮬레이터.
  *Bioinformatics*, 39:btad540. <https://doi.org/10.1093/bioinformatics/btad540>

아미노산 Q 행렬을 추정하는 경우 다음을 인용하십시오.

* B.Q. Minh, C. Cao Dang, L.S. Vinh, R. Lanfear (2021)
  QMaker: 단백질 진화의 경험적 모델을 추정하는 빠르고 정확한 방법.
  _Syst. Biol._, 70:1046–1060. <https://doi.org/10.1093/sysbio/syab010>

이종분포 GHOST 모델 "+H"를 사용하는 경우 다음을 인용하십시오.

* S.M. Crotty, B.Q. Minh, N.G. Bean, B.R. Holland, J. Tuke, L.S. Jermiin, A. von Haeseler (2020)
  GHOST: 이종분포적으로 진화한 염기 서열 정렬에서 역사적 신호 복구.
  _Syst. Biol._, 69:249-264. <https://doi.org/10.1093/sysbio/syz051>

대칭성 테스트를 사용하는 경우 다음을 인용하십시오.

* S. Naser-Khdour, B.Q. Minh, W. Zhang, E.A. Stone, R. Lanfear (2019) 
  계통 발생 분석에서 모델 위반의 유병률 및 영향.
  *Genome Biol. Evol.*, 11:3341-3352. <https://doi.org/10.1093/gbe/evz193>

다형성 인식 모델을 사용하는 경우 다음을 인용하십시오.

* D. Schrempf, B.Q. Minh, A. von Haeseler, C. Kosiol (2019) 
  고급 돌연변이 모델, 부트스트랩 및 비율 이질성을 갖춘 다형성 인식 종 트리.
  *Mol. Biol. Evol.*, 36:1294–1301. <https://doi.org/10.1093/molbev/msz043>

초고속 부트스트랩(UFBoot)의 경우 다음을 인용하십시오.

* D.T. Hoang, O. Chernomor, A. von Haeseler, B.Q. Minh, and L.S. Vinh (2018) 
  UFBoot2: 초고속 부트스트랩 근사 개선.
  *Mol. Biol. Evol.*, 35:518–522. <https://doi.org/10.1093/molbev/msx281>

사후 평균 사이트 빈도 모델(PMSF)을 사용하는 경우 다음을 인용하십시오.

* H.C. Wang, B.Q. Minh, S. Susko, A.J. Roger (2018) 
  사후 평균 사이트 빈도 프로파일을 사용한 사이트 이질성 모델링은 정확한 계통유전체학적 추정을 가속화합니다.
  *Syst. Biol.*, 67:216–235. <https://doi.org/10.1093/sysbio/syx068>

ModelFinder를 사용하는 경우 다음을 인용하십시오.

* S. Kalyaanamoorthy, B.Q. Minh, T.K.F. Wong, A. von Haeseler, L.S. Jermiin (2017) 
  ModelFinder: 정확한 계통 발생 추정을 위한 빠른 모델 선택.
  *Nat. Methods*, 14:587-589. <https://doi.org/10.1038/nmeth.4285>

분할 모델을 사용하는 경우 다음을 인용하십시오.

* O. Chernomor, A. von Haeseler, B.Q. Minh (2016) 
  슈퍼매트릭스로부터 계통유전체학적 추론을 위한 테라스 인식 데이터 구조.
  *Syst. Biol.*, 65:997-1008. <https://doi.org/10.1093/sysbio/syw037>

IQ-TREE 웹 서버를 사용하는 경우 다음을 인용하십시오.

* J. Trifinopoulos, L.-T. Nguyen, A. von Haeseler, B.Q. Minh (2016) 
  W-IQ-TREE: 최대 가능도 분석을 위한 빠른 온라인 계통 발생 도구.
  *Nucleic Acids Res.*, 44:W232-W235. <https://doi.org/10.1093/nar/gkw256>

IQ-TREE 버전 1을 사용하는 경우 다음을 인용하십시오.

* L. Nguyen, H.A. Schmidt, A. von Haeseler, B.Q. Minh (2015)
  IQ-TREE: 최대 가능도 계통수를 추정하기 위한 빠르고 효과적인 확률적 알고리즘.
  _Mol. Biol. and Evol._, 32:268-274. <https://doi.org/10.1093/molbev/msu300>

#### 크레딧 및 감사의 말

코드의 일부는 다음 패키지/라이브러리에서 가져왔습니다: [Phylogenetic likelihood library](http://www.libpll.org), [TREE-PUZZLE](http://www.tree-puzzle.de),
[BIONJ](http://dx.doi.org/10.1093/oxfordjournals.molbev.a025808), [Nexus Class Libary](http://dx.doi.org/10.1093/bioinformatics/btg319), [Eigen library](http://eigen.tuxfamily.org/),
[SPRNG library](http://www.sprng.org), [Zlib library](http://www.zlib.net), [gzstream library](http://www.cs.unc.edu/Research/compgeom/gzstream/), [vectorclass library](http://www.agner.org/optimize/), [GNU scientific library](https://www.gnu.org/software/gsl/).


IQ-TREE는 [오스트리아 과학 기금 - FWF](http://www.fwf.ac.at/)
(2012-2015년 보조금 번호 I 760-B17 및 2016-2019년 보조금 번호 I 2508-B29),
[비엔나 대학교](https://www.univie.ac.at/) (Initiativkolleg I059-N),
[호주 국립 대학교](https://www.anu.edu.au),
[챈 저커버그 이니셔티브](https://chanzuckerberg.com) (과학 보조금을 위한 오픈 소스 소프트웨어),
[사이먼스 재단](https://www.simonsfoundation.org), [무어 재단](https://www.moore.org),
및 [호주 연구 위원회](https://www.arc.gov.au)의 지원을 받았습니다.


[Anisimova et al., 2011]: http://dx.doi.org/10.1093/sysbio/syr041
[Guindon et al., 2010]: http://dx.doi.org/10.1093/sysbio/syq010
[Kalyaanamoorthy et al., 2017]: https://doi.org/10.1038/nmeth.4285
[Ly-Trong et al., 2023]: https://doi.org/10.1093/bioinformatics/btad540
[Minh et al., 2013]: http://dx.doi.org/10.1093/molbev/mst024
[Nguyen et al., 2015]: http://dx.doi.org/10.1093/molbev/msu300
[Shimodaira, 2002]: http://dx.doi.org/10.1080/10635150290069913
