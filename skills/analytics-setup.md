# Analytics Setup Skill

KPI definitions, tracking setup instructions, UTM parameters, ESP metrics, LinkedIn analytics for the funnel-architect agent.

## Core KPIs by Funnel Stage

### Awareness Stage
| KPI | Definition | Target |
|-----|-----------|--------|
| Impressions | Times content displayed | Platform-dependent |
| Reach | Unique accounts that saw content | Platform-dependent |
| Engagement rate | (Likes + Comments + Shares) / Impressions | >2% good, >5% great |
| Click-through rate | Clicks / Impressions | >0.5% good, >1% great |

### Opt-in Stage
| KPI | Definition | Target |
|-----|-----------|--------|
| Landing page views | Unique landing page visitors | — |
| Opt-in rate | Opt-ins / Landing page views | >3% good, >8% great |
| Bounce rate | Single-page visits / Total visits | <50% good, <30% great |
| Time on page | Average time spent | >30s good, >90s great |

### Email Stage
| KPI | Definition | Target |
|-----|-----------|--------|
| Delivery rate | Delivered / Sent | >95% |
| Open rate | Opened / Delivered | >20% good, >35% great |
| Click rate | Clicked / Delivered | >2% good, >5% great |
| Unsubscribe rate | Unsubscribed / Delivered | <0.2% |

### Conversion Stage
| KPI | Definition | Target |
|-----|-----------|--------|
| Offer page views | Unique visitors to offer | — |
| Conversion rate | Purchases / Offer page views | >2% good, >5% great |
| Revenue | Number of sales × price | — |
| Cost per acquisition | Spend / Number of customers | <30% of customer LTV |

## UTM Parameter Setup

### Standard UTM Structure
```
?utm_source=[platform]&utm_medium=[channel]&utm_campaign=[campaign-name]&utm_content=[specific-content]
```

### Platform Mappings
| Platform | utm_source value |
|----------|-----------------|
| LinkedIn | linkedin |
| X/Twitter | twitter |
| Instagram | instagram |
| Facebook | facebook |
| Email newsletter | email |
| Cold email | cold-email |

### Medium Mappings
| Channel | utm_medium value |
|---------|-----------------|
| Social post | social-post |
| Social ad | social-ad |
| Email | email |
| Cold email | cold-email |
| Organic | organic |
| Referral | referral |

### Campaign Naming
Format: YYYY-MM-DD-campaign-name-content-type

Examples:
- 2026-01-15-launchsuite-linkedin-post
- 2026-01-20-funnellinkedin-ad
- 2026-02-01-newsletter-week5

## Tracking Setup

### Google Analytics 4
1. Create GA4 property
2. Install tracking code on landing page
3. Set up conversions for:
   - Lead magnet opt-in (form submit)
   - Offer purchase (thank you page)
4. Set up custom audiences based on behavior

### UTM Tracking in URLs
All traffic sources must use UTM parameters:
- Landing page links in social posts
- Email links
- Any external link pointing to landing page

### Email ESP Analytics
ConvertKit / ActiveCampaign metrics to track:
- Tag-based segment performance
- Sequence engagement by tag
- Link click heatmaps
- Unsubscribe reasons (if available)

### LinkedIn Analytics
Track at campaign level:
- Impressions, clicks, CTR by post
- Engagement rate trend
- Follower growth
- Visitor demographics

### Facebook Pixel (if running ads)
Events to track:
- PageView (landing page)
- Lead (opt-in)
- Purchase (if applicable)

## Dashboard Setup

### Minimum Viable Dashboard
Weekly metrics to review:
1. Landing page: views, opt-ins, opt-in rate
2. Email: opens, clicks, unsubscribes
3. Social: engagement rate, follower growth
4. Revenue: sales, revenue

### Attribution Model
Simple first-touch attribution:
- Which content drove the first interaction?
- Which platform generated the lead?

Complex multi-touch (if tools allow):
- Weight across touchpoints
- Time-decay model

## Quality Checklist

- [ ] UTM parameters on all external links
- [ ] GA4 or equivalent installed on landing page
- [ ] Email ESP tracking configured
- [ ] Conversion events set up
- [ ] Dashboard created with weekly review cadence
- [ ] Benchmark metrics defined for each KPI