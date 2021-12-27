<template>
  <AboutMeWrapper>
    <Introduction>
      <Title>Introduction</Title>
      <Content>
        <P> Technology, management, innovation and design enthusiast. </P>
        <P>
          Software Manager at <b>loomi</b>; Graduation student in Computer
          Engineering at CIn / UFPE and Computer Technician at IFRN.
        </P>
        <P>
          Working with management and development of software projects, using
          agile methodologies, management strategies and evolution of digital
          products, software architecture and software maintenance techniques.
        </P>
        <P>
          Interested in software development, agile, project management, product
          management, people development and experience, devops, software
          infrastructure, software architecture, code design, security and
          software privacy.
        </P>
      </Content>
    </Introduction>
    <Experiences>
      <Title>Experiences</Title>
      <TimelineEvent
        role="Software Manager"
        time="Now (since 2021.2)"
        company="at loomi"
      />
      <TimelineEvent
        role="Software Developer"
        time="6 months (since 2021.1)"
        company="at loomi"
      />
      <TimelineEvent
        role="Software Manager"
        time="1 year (2020)"
        company="at CITi"
      />
      <TimelineEvent
        role="Software Developer"
        time="6 months (2019.2)"
        company="at CITi"
      />
    </Experiences>

    <Technologies>
      <Title>Technologies</Title>
      <TagsWrapper>
        <Tag>Javascript</Tag>
        <Tag>Python</Tag>
        <Tag>React</Tag>
        <Tag>Node.js</Tag>
        <Tag>Django</Tag>
        <Tag>HTML</Tag>
        <Tag>SASS</Tag>
        <Tag>MongoDB</Tag>
        <Tag>PostgreSQL</Tag>
        <Tag>MySQL</Tag>
        <Tag>Git</Tag>
        <Tag>Django</Tag>
        <Tag>Java</Tag>
        <Tag>Play Framework</Tag>
        <Tag>C</Tag>
        <Tag>AWS Services</Tag>
        <Tag>Docker</Tag>
        <Tag>Dokku</Tag>
        <Tag>Linux</Tag>
      </TagsWrapper>
    </Technologies>

    <Knowledge>
      <Title>Knowledge</Title>
      <TagsWrapper>
        <Tag light>Software Development</Tag>
        <Tag light>Project Management</Tag>
        <Tag light>Agile</Tag>
        <Tag light>Leadership</Tag>
      </TagsWrapper>
    </Knowledge>

    <Ornament :src="require('../assets/icons/ornament1.svg')" />
    <WaterMark>ABOUT ME</WaterMark>
  </AboutMeWrapper>
</template>

<script>
import styled from 'vue-styled-components';
import TimelineEvent from './TimelineEvent.vue';
import { Theme, WaterMark, TagsWrapper, Tag } from '../assets/style';

const AboutMeWrapper = styled.section`
  position: relative;
  width: 100%;
  background-color: #1b1b1b;
  background-image: linear-gradient(to right, #292828, #1b1b1b);
  padding: 6rem 4rem;
  display: grid;
  grid-template-areas:
    'introduction introduction'
    'experiences technologies'
    'experiences knowledge';
  grid-template-columns: 1fr 2fr;
  grid-gap: 2rem 4rem;
  overflow: hidden;

  @media (max-width: 1024px) {
    padding: 6rem 2rem;
    grid-template-columns: 1fr;
    grid-template-areas:
      'introduction'
      'experiences'
      'technologies'
      'knowledge';
  }
`;

const Title = styled.h2`
  font: ${Theme.font.subtitle};
  color: ${Theme.color.lightGray};
  margin: 0 0 1rem 0;
`;

const Introduction = styled.div`
  grid-area: introduction;
`;

const Content = styled.p`
  font: ${Theme.font.text};
  color: ${Theme.color.lightGray};
  text-justify: none;
  width: 92.5%;
`;

const Experiences = styled.div`
  grid-area: experiences;
`;

const Technologies = styled.div`
  grid-area: technologies;
`;

const Knowledge = styled.div`
  grid-area: knowledge;
`;

const Ornament = styled.img`
  position: absolute;
  top: 6rem;
  right: -5rem;
  width: 20vw;
  min-width: 17.5rem;
`;

const P = styled.p`
  padding-bottom: 1rem;
`;

export default {
  name: 'AboutMe',
  components: {
    AboutMeWrapper,
    Title,
    TagsWrapper,
    Tag,
    WaterMark,
    Introduction,
    Content,
    Experiences,
    Technologies,
    Knowledge,
    TimelineEvent,
    Ornament,
    P,
  },
};
</script>
