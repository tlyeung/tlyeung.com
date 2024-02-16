+++
title = 'Universal Testing'
date = 2024-02-16T00:01:11+08:00
draft = true
+++

Universal Testing has been a topic in Hong Kong for a few days. Doctors and medical professors, including the prominent microbiologist Yuen Kwok Yung, doubted. [Dr Yuen said it can only be possible if we can test all 8 million population in Hong Kong in 4 or 5 days.](https://news.mingpao.com/pns/%E8%A6%81%E8%81%9E/article/20200803/s00001/1596392381166/%E6%87%89%E5%90%A6%E5%85%A8%E6%B0%91%E6%AA%A2%E6%B8%AC-%E8%A2%81%E5%9C%8B%E5%8B%87-%E5%8F%AF%E5%90%A65%E6%97%A5%E9%A9%97750%E8%90%AC%E4%BA%BA) My question is, even if we can handle 2 million testings a day, is it a good approach?

To get millions of test results, we probably will need to use test kits that made in China. Because the amount of antibodies varies, the test result will not be 100% accurate. [Some Chinese test kits have a accuracy as low as only 90%](https://news.rthk.hk/rthk/en/component/k2/1513995-20200312.htm). Let's make it 95% accurate for both positive and negative.

Here we have the total accuracies:

|positive|false positive|
|---|---|
|95%|5%|

|negative|false negative|
|---|---|
|95%|5%	|

Let's assume 80,000 of Hong Kong citizens are infected. After we would have tested all 8 millions, how many of the infected people can we identify? Easy, 80,000 x 95% = 76,000. **WRONG!** There will be also 5% false positive for the uninfected 7,920,000 people. So there will be 7,920,000 x 0.05 + 80,000 x 0.95 = a jaw dropping 472,000 people!!! 

It's unlikely to have such a high false positive rate, while as we have read in the news, some patients may not have a high degree of virus or antibodies for accurate negative tests, so let's change the accuracy assumptions as below. It would be the **ideal** case.

|positive|false positive|
|---|---|
|99.9%|0.1%|

|negative|false negative|
|---|---|
|99%|1%	|

We will find 7,920,000 x 0.001 + 80,000 x 0.99 = 87,120 people infected. But among them, only 80,000 x 0.99/87,120 = 90.9% are really infected. Almost 10% are false positive cases. While 1%, 800 infected people will test negative! The figures I used were **ideal** already!

You may [learn more about Bayes' Theorem](https://en.wikipedia.org/wiki/Bayes%27_theorem). You can also listen to the [podcast of famous mathematician and radio presenter Hannah Fry](https://www.numberphile.com/videos/podcast-hannah-fry-coronavirus), from 9:05.

As a result I can conclude that, universal testing is useless. It will find many false positive cases, while hundreds false negative cases will be missed.

So what are the right moves? Here are my suggestions.

1. We test all patients who thought they have got the virus, even with very mild symptoms. So we can detect the newly infected cases and isolate them as soon as possible.
2. We test the correlations of the confirm cases sooner the better, obviously they are more likely to be infected than any others.
3. We keep testing high risk population. Such as staff in hospitals, nurses, doctors, etc. If they have got the virus, they will infect the most vulnerable people.
4. Start random testings. Let's test 500 people randomly, from all walks of life. It will give us a basic idea how the virus spreads in the community. We can do this on monthly basis.

