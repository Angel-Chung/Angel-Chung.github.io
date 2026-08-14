---
layout: page
title: research
permalink: /publications/
nav: true
nav_order: 3
---

<style>
.research-list {
  padding-left: 20px;
}

.research-list > li {
  margin-bottom: 1.45rem;
}

h2 {
  font-size: 1.35rem;
  line-height: 1.3;
  margin: 1.2em 0 0.6em;
}

.paper-title {
  font-weight: 600;
  text-decoration: none;
  color: var(--global-theme-color);
}

.paper-title:hover {
  text-decoration: underline;
}

.paper-title-line {
  display: block;
  line-height: 1.4;
}

.paper-title-plain {
  color: var(--global-text-color);
  font-weight: 600;
}

.paper-authors {
  color: var(--global-text-color-light);
  color: color-mix(in srgb, var(--global-text-color) 72%, var(--global-bg-color));
  font-size: 0.91rem;
  line-height: 1.45;
  margin-top: 0.18rem;
}

.paper-authors strong {
  color: inherit;
  font-weight: 500;
}

.author-order-note {
  font-size: 0.82em;
}

.paper-venue {
  color: color-mix(in srgb, var(--global-text-color) 82%, var(--global-bg-color));
  font-size: 0.91rem;
  line-height: 1.45;
  margin-top: 0.1rem;
}

.paper-venue strong {
  color: inherit;
  font-weight: 500;
}

.paper-note {
  color: var(--global-text-color-light);
  color: color-mix(in srgb, var(--global-text-color) 72%, var(--global-bg-color));
  display: block;
  font-size: 0.82rem;
  line-height: 1.35;
  margin-top: 0.08rem;
}

.paper-actions {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 0.36rem;
  margin-top: 0.5rem;
}

.paper-button,
.paper-news > summary,
.paper-abstract > summary {
  --paper-action-color: #d783a2;

  align-items: center;
  background-color: transparent;
  border: 1px solid color-mix(in srgb, var(--paper-action-color) 42%, var(--global-divider-color));
  border-radius: 0.28rem;
  box-shadow: none;
  color: color-mix(in srgb, var(--global-text-color) 74%, var(--paper-action-color));
  display: inline-flex;
  font-size: 0.76rem;
  font-weight: 450;
  justify-content: center;
  line-height: 1.2;
  min-height: 1.48rem;
  padding: 0.22rem 0.56rem;
  text-decoration: none;
  transition:
    border-color 150ms ease,
    box-shadow 150ms ease,
    color 150ms ease;
}

.paper-news > summary,
.paper-abstract > summary {
  --paper-action-color: #79a9d6;
}

.paper-button:hover,
.paper-news > summary:hover,
.paper-abstract > summary:hover {
  background-color: transparent;
  border-color: color-mix(in srgb, var(--paper-action-color) 68%, var(--global-divider-color));
  box-shadow: 0 0.16rem 0.42rem rgba(0, 0, 0, 0.05);
  color: color-mix(in srgb, var(--global-text-color) 62%, var(--paper-action-color));
  text-decoration: none;
}

.paper-button:focus-visible,
.paper-news > summary:focus-visible,
.paper-abstract > summary:focus-visible {
  border-color: color-mix(in srgb, var(--paper-action-color) 70%, var(--global-text-color));
  box-shadow: 0 0 0 0.12rem color-mix(in srgb, var(--paper-action-color) 24%, transparent);
  outline: none;
}

.paper-button:focus,
.paper-news > summary:focus,
.paper-abstract > summary:focus {
  outline: none;
}

.paper-button-disabled {
  background-color: transparent;
  border-color: transparent;
  color: var(--global-text-color-light);
  cursor: not-allowed;
  opacity: 0.72;
}

.paper-button-disabled:hover {
  background-color: transparent;
  border-color: transparent;
  box-shadow: none;
  color: var(--global-text-color-light);
}

.paper-abstract {
  display: contents;
  margin: 0;
}

.paper-news {
  display: inline-flex;
  margin: 0;
  position: relative;
  z-index: 1;
}

.paper-news[open] {
  z-index: 10;
}

.paper-news[open] > summary {
  background-color: transparent;
  border-color: color-mix(in srgb, var(--paper-action-color) 72%, var(--global-divider-color));
  color: color-mix(in srgb, var(--global-text-color) 58%, var(--paper-action-color));
}

.paper-news > summary,
.paper-abstract > summary {
  cursor: pointer;
  list-style: none;
}

.paper-news > summary::-webkit-details-marker,
.paper-abstract > summary::-webkit-details-marker {
  display: none;
}

.paper-news > summary::after,
.paper-abstract > summary::after {
  border-bottom: 1.5px solid currentColor;
  border-right: 1.5px solid currentColor;
  content: "";
  height: 0.28rem;
  margin-left: 0.35rem;
  transform: rotate(45deg) translateY(-0.08rem);
  transition: transform 150ms ease;
  width: 0.28rem;
}

.paper-news[open] > summary::after,
.paper-abstract[open] > summary::after {
  transform: rotate(225deg) translate(-0.03rem, -0.03rem);
}

.paper-abstract-panel {
  border-left: 3px solid var(--global-theme-color);
  flex: 0 0 100%;
  margin-top: 0.55rem;
  padding: 0.05rem 0 0.05rem 0.9rem;
}

.paper-news-panel {
  background-color: var(--global-bg-color);
  border: 1px solid var(--global-divider-color);
  border-radius: 0.35rem;
  box-shadow: 0 0.7rem 1.45rem rgba(0, 0, 0, 0.12);
  left: 0;
  margin-top: 0;
  max-width: min(22rem, calc(100vw - 2rem));
  min-width: 16rem;
  padding: 0.55rem 0.65rem;
  position: absolute;
  top: calc(100% + 0.5rem);
  width: max-content;
}

.paper-news-list {
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.paper-news-link {
  border-radius: 0.32rem;
  display: flex;
  flex-direction: column;
  gap: 0.08rem;
  line-height: 1.4;
  padding: 0.22rem 0.28rem;
  text-decoration: none;
}

.paper-news-source {
  color: var(--global-text-color);
  font-size: 0.9rem;
  font-weight: 500;
}

.paper-news-detail {
  color: var(--global-text-color-light);
  color: color-mix(in srgb, var(--global-text-color) 72%, var(--global-bg-color));
  font-size: 0.84rem;
}

.paper-news-link:hover .paper-news-source {
  color: var(--global-theme-color);
}

.paper-news-link:hover {
  background-color: transparent;
  text-decoration: none;
}

.paper-abstract-panel p {
  font-size: 0.94rem;
  line-height: 1.55;
  margin-bottom: 0;
}

.section-space {
  margin-top: 40px;
}

@media (max-width: 575.98px) {
  .research-list {
    padding-left: 1.1rem;
  }

  .paper-actions {
    gap: 0.35rem;
  }

  .paper-news {
    display: inline-flex;
    position: relative;
  }

  .paper-news[open] {
    display: flex;
    flex: 0 0 100%;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: flex-start;
  }

  .paper-news-panel {
    background-color: transparent;
    border: 0;
    border-left: 3px solid var(--global-theme-color);
    box-shadow: none;
    flex: 0 0 100%;
    margin-top: 0.55rem;
    max-width: none;
    min-width: 0;
    padding: 0.05rem 0 0.05rem 0.9rem;
    position: static;
    width: 100%;
  }
}
</style>

<h2>Journal Publication</h2>

<ul class="research-list">
  <li>
    <span class="paper-title-line"><a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4880140" class="paper-title">Improving Access to Essential Medicines via Decision-Aware Machine Learning</a></span>
    <div class="paper-authors"><strong>Chung, A. T.-H.</strong>, Abdulai, J., Bayoh, P., Sandi, L., Smart, F., Bastani*, H., Bastani*, O. (2026).</div>
    <div class="paper-venue"><i><strong>Nature</strong> 653, 1178–1183 (research article)</i>.</div>
    <small class="paper-note">*denote equal last author</small>
    <div class="paper-actions" aria-label="Paper links">
      <a class="paper-button" href="https://www.nature.com/articles/s41586-026-10433-7" target="_blank" rel="noopener">Nature</a>
      <a class="paper-button" href="https://www.nature.com/articles/d41586-026-01152-0" target="_blank" rel="noopener">Nature News</a>
      <a class="paper-button" href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4880140" target="_blank" rel="noopener">SSRN</a>
      <a class="paper-button" href="https://communities.springernature.com/posts/behind-the-paper-deploying-decision-aware-learning-for-real-world-health-systems" target="_blank" rel="noopener">Behind the Paper</a>
      <details class="paper-news">
        <summary>Media Coverage</summary>
        <div class="paper-news-panel">
          <ul class="paper-news-list">
            <li>
              <a class="paper-news-link" href="https://www.nature.com/articles/d41586-026-01152-0" target="_blank" rel="noopener">
                <span class="paper-news-source">Nature News</span>
                <span class="paper-news-detail">Research highlight</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://analytics.wharton.upenn.edu/news/research-spotlight-angel-chung/" target="_blank" rel="noopener">
                <span class="paper-news-source">Wharton AI & Analytics</span>
                <span class="paper-news-detail">Research spotlight</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://penntoday.upenn.edu/news/transforming-healthcare-logistics-low-cost-ai" target="_blank" rel="noopener">
                <span class="paper-news-source">Penn Today</span>
                <span class="paper-news-detail">Transforming healthcare logistics with low-cost AI</span>
              </a>
            </li>
          </ul>
        </div>
      </details>
      <details class="paper-abstract">
        <summary>Abstract</summary>
        <div class="paper-abstract-panel">
          <p>A critical challenge in healthcare systems in low- and middle-income countries (LMICs) is the efficient and equitable allocation of scarce resources, particularly essential medicines. This problem is complicated by limited high-quality data, which restricts the applicability of traditional data-driven techniques. We propose a novel decision-aware machine learning framework for essential medicines allocation, which additionally leverages multi-task learning to ensure sample efficiency and catalytic priors to ensure equitable allocation. In collaboration with the Sierra Leone national government, we performed a staggered, nationwide deployment of our system as a decision support tool. Our econometric evaluation finds an estimated 19% increase in consumption of allocated products in treated districts, demonstrating its efficacy at improving access to essential medicines. Our tool was subsequently scaled nationwide, covering an estimated 2 million women and children under five. Our work demonstrates how machine learning methods can improve efficiency at very low cost in resource-constrained global health settings.</p>
        </div>
      </details>
    </div>
  </li>
</ul>

<h2>Working Papers</h2>
<ul class="research-list">
  <li>
    <span class="paper-title-line"><a href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6423358" class="paper-title">Effective Personalized AI Tutors via LLM-Guided Reinforcement Learning</a></span>
    <div class="paper-authors"><strong>Chung, A. T.-H.</strong>, Zhang, B., Kung, L.-C., Bastani*, H., and Bastani*, O.</div>
    <div class="paper-venue"><i>Available at SSRN.</i></div>
    <small class="paper-note">*denote equal last author</small>
    <div class="paper-actions" aria-label="Paper links">
      <a class="paper-button" href="https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6423358" target="_blank" rel="noopener">SSRN</a>
      <details class="paper-news">
        <summary>Media Coverage</summary>
        <div class="paper-news-panel">
          <ul class="paper-news-list">
            <li>
              <a class="paper-news-link" href="https://mackinstitute.wharton.upenn.edu/2026/research-spotlight-bastani-chung/" target="_blank" rel="noopener">
                <span class="paper-news-source">Mack Institute</span>
                <span class="paper-news-detail">Research spotlight</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://hechingerreport.org/proof-points-ai-tutor-python/" target="_blank" rel="noopener">
                <span class="paper-news-source">The Hechinger Report</span>
                <span class="paper-news-detail">Proof Points</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://knowledge.wharton.upenn.edu/article/how-personalized-ai-tutors-can-help-students-learn/" target="_blank" rel="noopener">
                <span class="paper-news-source">Knowledge at Wharton</span>
                <span class="paper-news-detail">How personalized AI tutors can help students learn</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://ai-analytics.wharton.upenn.edu/insights/why-better-ai-tutors-arent-about-better-answers/" target="_blank" rel="noopener">
                <span class="paper-news-source">Wharton AI & Analytics</span>
                <span class="paper-news-detail">Why better AI tutors aren't about better answers</span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://garyliang.substack.com/p/3-2-1-on-ai-and-learning-adaptive" target="_blank" rel="noopener">
                <span class="paper-news-source">3-2-1 on AI and learning adaptive</span>
                <span class="paper-news-detail"></span>
              </a>
            </li>
            <li>
              <a class="paper-news-link" href="https://www.linkedin.com/posts/edtech-aiineducation-adaptivelearning-ugcPost-7464768372988350464-8j6Y/" target="_blank" rel="noopener">
                <span class="paper-news-source">EdTech Insider</span>
                <span class="paper-news-detail">EdTech, AI in education, adaptive learning</span>
              </a>
            </li>
          </ul>
        </div>
      </details>
      <details class="paper-abstract">
        <summary>Abstract</summary>
        <div class="paper-abstract-panel">
          <p>Generative AI (GenAI) is rapidly reshaping education by unlocking the potential for personalized tutoring. Yet, emerging platforms largely focus on GenAI chatbot tutors that reactively answer student questions. We hypothesize that the efficacy of GenAI chatbot tutors can be substantially improved by proactively guiding student learning. To test this, we design a novel tutoring platform that tightly integrates a carefully-designed GenAI chatbot with a reinforcement learning algorithm for sequencing practice problems. Critically, this algorithm leverages rich signals from student-chatbot interactions to adaptively select practice problems of an appropriate difficulty level. In partnership with the Taipei City Government and American Institute in Taiwan, we deployed our tutoring platform in conjunction with a five-month course to teach Python to students across ten high schools. We randomized students between a fixed practice problem sequence and our adaptive sequencing algorithm. We find that adaptive sequencing increased unassisted final exam performance by 0.15 standard deviations (equivalent to 6-9 months of schooling by some estimates); mediation analysis suggests that gains were driven by increased engagement. Our work provides large-scale field evidence that student-chatbot interactions provide valuable signals for proactively optimizing and personalizing student learning.</p>
        </div>
      </details>
    </div>
  </li>
  <li>
    <span class="paper-title-line paper-title-plain">The Impact of Human-AI Collaboration in Outpatient Care: Evidence from Somaliland</span>
    <div class="paper-authors"><strong>Chung, A. T.-H.</strong>, Qin, J., Lin, P.-C., and Bastani, H.</div>
    <div class="paper-venue"><i>Draft available on request.</i></div>
    <details class="paper-abstract">
      <summary>Abstract</summary>
      <div class="paper-abstract-panel">
        <p>Healthcare documentation is one of the major operational burdens in resource-constrained health systems, often competing directly with patient care. This paper evaluates a human-AI collaborative documentation tool implemented at the largest public hospital in Somaliland. Physicians enter a clinical note draft, from which AI generates a polished clinical note that physicians may directly submit, edit then submit, or abandon AI note and submit their own draft. Exploiting the staggered rollout of this tool across hospital departments, we estimate intent-to-treat (ITT) effects using a Callaway and Sant’Anna (2021) difference-in-differences design. Our results show that AI significantly reduces service time by 34% and reduces service time dispersions across encounters. These findings suggest that AI has the potential to increase effective service capacity and standardize care delivery. We find no evidence that these gains come at the expense of clinical care quality. In particular, provider surveys indicate greater patient interaction and clinical note quality improves substantially. However, AI-enabled faster service do not necessarily improve patient access and downstream operational benefits, for example, patient waiting time does not decrease significantly. We show that this is because physicians strategically respond to the reduced service time by shortening total working time and by starting clinical day later. Furthermore, we find significant improvement on physicians’ independently written notes (without AI) post-treatment, suggesting that improvement does not necessarily require adoption; exposure to AI (but without adoption) can be of great value as well.</p>
      </div>
    </details>
  </li>
  <li>
    <span class="paper-title-line paper-title-plain">Grand Challenges for Operations Management: UN Sustainable Development Goal 3</span>
    <div class="paper-authors">Bastani, H., <strong>Chung, A. T.-H.</strong>, Joen, H., Yadav, P. <span class="author-order-note">(alphabetical)</span></div>
    <div class="paper-venue"><i>Minor Revision, Manufacturing &amp; Service Operations Management.</i></div>
  </li>
  <li>
    <span class="paper-title-line paper-title-plain">Incentive-Compatible Human-AI Collaboration via Adversarial Tasks</span>
    <div class="paper-authors">Bastani, H., Bastani, O., and <strong>Chung, A. T.-H.</strong> <span class="author-order-note">(alphabetical)</span></div>
    <div class="paper-venue"><i>Draft under preparation.</i></div>
  </li>
</ul>

<h2 class="section-space">Refereed Conference Papers</h2>
<ul class="research-list">
  <li>
    <span class="paper-title-line"><a href="https://arxiv.org/abs/2211.08507" class="paper-title">Decision-Aware Learning for Optimizing Health Supply Chains</a></span>
    <div class="paper-authors"><strong>Chung, A. T.-H.</strong>, Rostami, V., Bastani, H., & Bastani, O. (2022).</div>
    <div class="paper-venue"><i>Machine Learning for Health (ML4H)</i>.</div>
    <div class="paper-actions" aria-label="Paper links">
      <a class="paper-button" href="https://arxiv.org/abs/2211.08507" target="_blank" rel="noopener">arXiv</a>
      <details class="paper-abstract">
        <summary>Abstract</summary>
        <div class="paper-abstract-panel">
          <p>We study the problem of allocating limited supply of medical resources in developing countries, in particular, Sierra Leone. We address this problem by combining machine learning (to predict demand) with optimization (to optimize allocations). A key challenge is the need to align the loss function used to train the machine learning model with the decision loss associated with the downstream optimization problem. Traditional solutions have limited flexibility in the model architecture and scale poorly to large datasets. We propose a decision-aware learning algorithm that uses a novel Taylor expansion of the optimal decision loss to derive the machine learning loss. Importantly, our approach only requires a simple re-weighting of the training data, ensuring it is both flexible and scalable, e.g., we incorporate it into a random forest trained using a multitask learning framework. We apply our framework to optimize the distribution of essential medicines in collaboration with policymakers in Sierra Leone; highly uncertain demand and limited budgets currently result in excessive unmet demand. Out-of-sample results demonstrate that our end-to-end approach can significantly reduce unmet demand across 1040 health facilities throughout Sierra Leone.</p>
        </div>
      </details>
    </div>
  </li>
</ul>


 <h2 class="section-space">Book Chapter</h2>

<ul class="research-list">
  <li>
    <span class="paper-title-line"><a href="https://doi.org/10.1007/978-3-031-60867-4_12" class="paper-title">Optimizing Health Supply Chains in LMICs with Machine Learning: A Case Study in Sierra Leone</a></span>
    <div class="paper-authors">Bastani, H., Bastani, O., and <strong>Chung, A. T.-H.</strong> <span class="author-order-note">(alphabetical)</span> (2024).</div>
    <div class="paper-venue">In C. S. Tang (Ed.), <i>Responsible and Sustainable Operations: The New Frontier</i> (pp. 187-202). Springer Nature Switzerland.</div>
    <div class="paper-actions" aria-label="Paper links">
      <a class="paper-button" href="https://doi.org/10.1007/978-3-031-60867-4_12" target="_blank" rel="noopener">Full Chapter</a>
      <details class="paper-abstract">
        <summary>Abstract</summary>
        <div class="paper-abstract-panel">
          <p>This chapter overviews the challenges in pharmaceutical supply chains (PSCs) in Low- and Middle-Income Countries (LMICs), with a focus on Sierra Leone. Furthermore, it describes how traditional supply chain optimization strategies can be used to improve performance of PSCs in Sierra Leone. Finally, it describes the significant potential for using machine learning in this framework for effective demand forecasting. We highlight challenges such as limited data availability, the need to ensure equitable distribution, as well as the potential for transfer learning to address some of these challenges.</p>
        </div>
      </details>
    </div>
  </li>
</ul>

<h2 class="section-space">Invited Paper</h2>
<ul class="research-list">
  <li>
    <span class="paper-title-line"><a href="https://www.icdf.org.tw/wSite/ct?xItem=73588&ctNode=31211&mp=1" class="paper-title">Application of AI in Healthcare Management in Developing Countries</a> <span>(in Chinese)</span></span>
    <div class="paper-authors"><strong>Chung, A. T.-H.</strong>. (2025).</div>
    <div class="paper-venue"><i>Development Focus Quarterly, Issue 20</i>.</div>
    <div class="paper-actions" aria-label="Paper links">
      <details class="paper-abstract">
        <summary>Abstract</summary>
        <div class="paper-abstract-panel">
          <p>Artificial intelligence (AI) is rapidly becoming a key technology for improving healthcare and public health services, especially in developing countries with limited medical resources. This article first integrates international reports and academic literature to summarize the core applications of AI in four areas: disease prevention, telemedicine, healthcare resource allocation, and health education. It then draws on the author’s field experience in Sierra Leone and Somaliland to explain how AI technologies such as decision-aware machine learning, large language models (LLMs), and reinforcement learning (RL) can substantially improve the efficiency and equity of healthcare services.</p>
          <p>Despite its promising prospects, challenges such as insufficient data, weak infrastructure, lack of funding and talent, and incomplete regulatory and ethical frameworks still limit the implementation of AI in resource-constrained settings. To realize the benefits of AI while avoiding risks such as data privacy violations, algorithmic bias, and the widening of healthcare inequality, future development should focus on strengthening infrastructure, cultivating local talent, and establishing appropriate regulatory policies to ensure the ethical and inclusive use of AI, and to achieve the goals of health equity and sustainable development.</p>
        </div>
      </details>
    </div>
  </li>
</ul>

<h2 class="section-space">Work In Progress</h2>
<ul class="research-list">
  <li>
    <span class="paper-title-line paper-title-plain">Human–AI Agentic Networks for Community Health in Somaliland</span>
    <div class="paper-authors">with Bastani, H. and Lin, P.-C.</div>
  </li>
  <li>
    <span class="paper-title-line paper-title-plain">Trust in AI for Resource Allocation Using Housing Images</span>
    <div class="paper-authors">with Harari, M. and Wong, M.</div>
  </li>
  <li>
    <span class="paper-title-line paper-title-plain">AI for Poverty Targeting</span>
    <div class="paper-authors">with Harari, M. and Wong, M.</div>
  </li>
</ul>
