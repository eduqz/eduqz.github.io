<template>
  <SidebarWrapper>
    <HightlightedText>EDUARDO ALMEIDA</HightlightedText>

    <SocialMedias>
      <a href="https://www.linkedin.com/in/eduardoaqz/" target="_blank">
        <Icon :src="require('../assets/icons/linkedin.svg')" />
      </a>
      <a href="https://github.com/eduqz" target="_blank">
        <Icon :src="require('../assets/icons/github.svg')" />
      </a>
      <a href="https://eduqz.medium.com/" target="_blank">
        <Icon :src="require('../assets/icons/medium.svg')" />
      </a>
    </SocialMedias>
  </SidebarWrapper>
</template>

<script>
import styled from 'vue-styled-components';
import { Theme } from '../assets/style';

const SidebarWrapper = styled.aside`
  background-color: ${Theme.color.darkGray};
  padding: 4rem 0.5rem;
  width: 5rem;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  z-index: 10;

  @media (max-width: 1024px) {
    width: 100%;
    height: 5rem;
    top: unset;
    bottom: 0;
    padding: 0 2rem;
    flex-direction: row;
  }
`;

const HightlightedText = styled.p`
  font: ${Theme.font.bigText};
  color: ${Theme.color.lightGray};
  writing-mode: vertical-rl;
  width: min-content;
  transform: scale(-1, -1);

  @media (max-width: 1024px) {
    writing-mode: unset;
    width: unset;
    transform: scale(1, 1);
  }
`;

const SocialMedias = styled.div`
  display: flex;
  flex-direction: column;

  @media (max-width: 1024px) {
    flex-direction: row;
  }
`;

const Icon = styled.img`
  margin-top: 1rem;
  height: 1.5rem;
  transition: all .1s ease-in-out;

  &:hover {
    transform: scale(1.2);
  }

  @media (max-width: 1024px) {
    margin: 0 0 0 1.5rem;
    height: 1.75rem;
  }
`;

export default {
  name: 'Sidebar',
  components: {
    SidebarWrapper,
    HightlightedText,
    SocialMedias,
    Icon,
  },
};
</script>
