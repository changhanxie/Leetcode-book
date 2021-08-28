# Prefix Sum And Difference Array

## Prefix Sum and Difference Array

{% hint style="info" %}
template 1: size = N, start from nums\[0\]
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
template 2: size = N + 1, start from nums\[1\], nums\[0\] = 0
{% endhint %}

```java
//size = N + 1
int[] sum = new int[N + 1];
for(int i = 0; i < N; i++){
    sum[i + 1] = sum[i] + nums[i]
}
```

#### Type: Two Sum

{% page-ref page="560.-subarray-sum-equals-k.md" %}

{% page-ref page="974.-subarray-sums-divisible-by-k.md" %}

#### Type: Range Sum

#### Type: Sliding Window

{% page-ref page="1200.-minimum-absolute-difference.md" %}

#### Type: Monotonic Queue



