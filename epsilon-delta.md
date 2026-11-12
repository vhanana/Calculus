# 엡실론-델타 논법: 함수의 극한을 엄밀하게 정의하기

## 1. 왜 필요한가요?

“\(x\)가 \(a\)에 가까워지면 \(f(x)\)는 \(L\)에 가까워진다”라는 설명은 직관적이지만, **얼마나 가까워야 하는지**를 명확하게 말하지 않습니다. 엡실론-델타(\(\varepsilon\)-\(\delta\)) 논법은 거리를 이용해 이를 엄밀하게 표현합니다.

## 2. 극한의 정의

함수 \(f\)가 \(a\)의 어떤 근방에서 \(a\) 자체를 제외하고 정의되어 있다고 합시다. 다음 조건이 성립하면

$$
\lim_{x\to a} f(x)=L
$$

이라고 합니다.

$$
\boxed{
\forall\varepsilon>0,\ \exists\delta>0\ \text{such that}\quad
0<|x-a|<\delta\ \Longrightarrow\ |f(x)-L|<\varepsilon
}
$$

- \(\varepsilon>0\): 함수값 \(f(x)\)와 극한값 \(L\) 사이에 허용하는 오차입니다.
- \(\delta>0\): 입력값 \(x\)와 \(a\) 사이에 허용하는 거리입니다.
- \(0<|x-a|\): \(x=a\)는 제외합니다. 따라서 극한은 \(f(a)\)의 값과 별개입니다.
- **양화사의 순서가 중요합니다.** 임의의 \(\varepsilon\)이 주어진 뒤, 그에 맞는 \(\delta\)를 정할 수 있어야 합니다.

쉽게 말해, **함수값의 오차를 아무리 작게 요구하더라도 입력값을 충분히 가까이 제한하여 그 요구를 만족시킬 수 있어야 한다**는 뜻입니다.

## 3. 간단한 증명

다음을 증명해 보겠습니다.

$$
\lim_{x\to 2}(3x+1)=7
$$

**증명.** 임의의 \(\varepsilon>0\)을 택합니다. 다음을 계산하면

$$
|(3x+1)-7|=3|x-2|
$$

입니다. 따라서 \(\delta=\varepsilon/3\)으로 정하면, \(0<|x-2|<\delta\)인 모든 \(x\)에 대해

$$
|(3x+1)-7|=3|x-2|<3\delta=\varepsilon
$$

가 성립합니다. 그러므로 엡실론-델타 정의에 의해

$$
\boxed{\lim_{x\to 2}(3x+1)=7}
$$

입니다. \(\square\)

## 4. 기억할 점

1. 먼저 임의의 \(\varepsilon>0\)을 설정합니다.
2. \(|f(x)-L|<\varepsilon\)을 보장할 \(\delta>0\)을 찾습니다.
3. \(0<|x-a|<\delta\)라는 가정에서 \(|f(x)-L|<\varepsilon\)을 증명합니다.

## 참고 자료

- OpenStax, *Calculus Volume 1*, §2.5, [The Precise Definition of a Limit](https://openstax.org/books/calculus-volume-1/pages/2-5-the-precise-definition-of-a-limit).
- APEX Calculus, §1.2, [Epsilon-Delta Definition of a Limit](https://opentext.uleth.ca/apex-calculus/sec_limit_def.html).
