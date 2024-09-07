<template>
  <section class="privacy-policy-area">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="privacy-policy-content">
            <h1 class="policy-title">Privacy Policy</h1>
            <p class="last-updated">Last Updated: September 7, 2024</p>

            <div class="policy-section">
              <h2>1. Information We Collect</h2>
              <p>We collect various types of information to provide and improve our services. The categories of personal information we may collect include:</p>
              <table class="info-table">
                <thead>
                <tr>
                  <th>Category</th>
                  <th>Examples</th>
                </tr>
                </thead>
                <tbody>
                <tr v-for="(row, index) in infoCategories" :key="index">
                  <td>{{ row.category }}</td>
                  <td>{{ row.examples }}</td>
                </tr>
                </tbody>
              </table>
            </div>

            <div class="policy-section">
              <h2>2. Use of Your Personal Information</h2>
              <p>We use the personal information we collect for various purposes, including:</p>
              <ul>
                <li>Providing, personalizing, and improving our services</li>
                <li>Communicating with you</li>
                <li>Processing transactions and sending related information</li>
                <li>Marketing and advertising our products and services</li>
                <li>Complying with legal obligations</li>
                <li>Protecting our rights and preventing fraud</li>
              </ul>
            </div>

            <div class="policy-section">
              <h2>3. How We Use Your Information</h2>
              <p>We use the information we collect to:</p>
              <ul>
                <li>Process donations and send receipts</li>
                <li>Communicate with you about our programs and events</li>
                <li>Improve our website and services</li>
                <li>Comply with legal obligations</li>
              </ul>
            </div>

            <div class="policy-section">
              <h2>4. Information Sharing and Disclosure</h2>
              <p>We do not sell or rent your personal information to third parties. We may share your information with:</p>
              <ul>
                <li>Service providers who assist in our operations</li>
                <li>Legal and regulatory authorities, when required by law</li>
              </ul>
            </div>

            <div class="policy-section">
              <h2>5. Data Security</h2>
              <p>We implement appropriate technical and organizational measures to protect your personal information. However, no method of transmission over the Internet is 100% secure.</p>
            </div>

            <div class="policy-section">
              <h2>6. Your Rights</h2>
              <p>You have the right to:</p>
              <ul>
                <li>Access your personal information</li>
                <li>Correct inaccurate information</li>
                <li>Request deletion of your information</li>
                <li>Opt-out of marketing communications</li>
              </ul>
            </div>

            <div class="policy-section">
              <h2>7. Children's Privacy</h2>
              <p>Our website is not intended for children under 13. We do not knowingly collect personal information from children under 13.</p>
            </div>

            <div class="policy-section">
              <h2>8. Changes to This Privacy Policy</h2>
              <p>We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page.</p>
            </div>

            <div class="policy-section">
              <h2>9. Contact Us</h2>
              <p>If you have any questions about this Privacy Policy, please contact us at:</p>
              <ul>
                <li>Email: privacy@ada.org</li>
                <li>Phone: +1 (123) 456-7890</li>
                <li>Address: 138 Tenth Avenue SW, Calgary, AB, Canada</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PrivacyPolicy',
  data() {
    return {
      infoCategories: [
        {
          category: 'A. Identifiers',
          examples: 'Contact details, such as real name, alias, postal address, telephone or mobile contact number, unique personal identifier, online identifier, Internet Protocol address, email address, and account name'
        },
        {
          category: 'B. Personal information as defined in the California Customer Records statute',
          examples: 'Name, contact information, education, employment, employment history, and financial information'
        },
        {
          category: 'C. Protected classification characteristics under state or federal law',
          examples: 'Gender, age, date of birth, race and ethnicity, national origin, marital status, and other demographic data'
        },
        {
          category: 'D. Commercial information',
          examples: 'Transaction information, purchase history, financial details, and payment information'
        },
        {
          category: 'E. Biometric information',
          examples: 'Fingerprints and voiceprints'
        },
        {
          category: 'F. Internet or other similar network activity',
          examples: 'Browsing history, search history, online behavior'
        },
        {
          category: 'G. Geolocation data',
          examples: 'Device location'
        },
        {
          category: 'H. Audio, electronic, visual, thermal, olfactory, or similar information',
          examples: 'Images and audio, video or call recordings created in connection with our business activities'
        },
        {
          category: 'I. Professional or employment-related information',
          examples: 'Business contact details, job title, work history, and professional qualifications if you apply for a job with us'
        },
        {
          category: 'J. Education Information',
          examples: 'Student records and directory information'
        },
        {
          category: 'K. Inferences drawn from other personal information',
          examples: 'Inferences drawn from any of the collected personal information listed above to create a profile or summary about, for example, an individual\'s preferences and characteristics'
        }
      ]
    }
  },
  mounted() {
    this.adjustPadding();
    window.addEventListener('resize', this.adjustPadding);
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.adjustPadding);
  },
  methods: {
    adjustPadding() {
      const footer = document.querySelector('footer');
      const content = document.querySelector('.privacy-policy-content');
      if (footer && content) {
        const footerHeight = footer.offsetHeight;
        content.style.paddingBottom = `${footerHeight}px`; // 60px extra space
      }
    }
  }
}
</script>

<style scoped>
.privacy-policy-area {
  padding: 60px 0 10px; /* Increased bottom padding to prevent footer overlap */
}
.policy-title {
  font-size: 2.5em;
  margin-bottom: 20px;
}
.last-updated {
  font-style: italic;
  margin-bottom: 30px;
}
.policy-section {
  margin-bottom: 30px;
}
.policy-section h2 {
  font-size: 1.8em;
  margin-bottom: 15px;
}
.policy-section p, .policy-section ul {
  margin-bottom: 15px;
}
.policy-section ul {
  padding-left: 20px;
}
.info-table {
  width: 100%;
  border-collapse: collapse;
  margin-bottom: 20px;
}
.info-table th, .info-table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}
.info-table th {
  background-color: #f2f2f2;
}
</style>