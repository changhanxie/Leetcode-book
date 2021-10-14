# Prefix Sum And Difference Array

## Prefix Sum and Difference Array

{% hint style="info" %}
template 1: size = N, start from nums\[0]
{% endhint %}

```java
//size = N
int[] sum = new int[nums.length];
sum[0] = nums[0];
for(int i = 1; i < nums.length; i++){
    sum[i] = sum[i - 1] + nums[i];
}
```

{% hint style="info" %}
template 2: size = N + 1, start from nums\[1], nums\[0] = 0
{% endhint %}

```java
//size = N + 1
int[] sum = new int[N + 1];
for(int i = 0; i < N; i++){
    sum[i + 1] = sum[i] + nums[i]
}
```

#### Type: Two Sum

{% content-ref url="53.-maximum-subarray.md" %}
[53.-maximum-subarray.md](53.-maximum-subarray.md)
{% endcontent-ref %}

{% content-ref url="525.-contiguous-array.md" %}
[525.-contiguous-array.md](525.-contiguous-array.md)
{% endcontent-ref %}

{% content-ref url="560.-subarray-sum-equals-k.md" %}
[560.-subarray-sum-equals-k.md](560.-subarray-sum-equals-k.md)
{% endcontent-ref %}

{% content-ref url="974.-subarray-sums-divisible-by-k.md" %}
[974.-subarray-sums-divisible-by-k.md](974.-subarray-sums-divisible-by-k.md)
{% endcontent-ref %}

{% content-ref url="1685.-sum-of-absolute-differences-in-a-sorted-array.md" %}
[1685.-sum-of-absolute-differences-in-a-sorted-array.md](1685.-sum-of-absolute-differences-in-a-sorted-array.md)
{% endcontent-ref %}

#### Type: Range Sum

#### Type: Sliding Window

{% content-ref url="209.-minimum-size-subarray-sum.md" %}
[209.-minimum-size-subarray-sum.md](209.-minimum-size-subarray-sum.md)
{% endcontent-ref %}

{% content-ref url="370.-range-addition.md" %}
[370.-range-addition.md](370.-range-addition.md)
{% endcontent-ref %}

{% content-ref url="1200.-minimum-absolute-difference.md" %}
[1200.-minimum-absolute-difference.md](1200.-minimum-absolute-difference.md)
{% endcontent-ref %}

{% content-ref url="untitled.md" %}
[untitled.md](untitled.md)
{% endcontent-ref %}

#### Type: Monotonic Queue

