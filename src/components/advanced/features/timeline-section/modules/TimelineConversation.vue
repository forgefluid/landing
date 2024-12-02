<script setup lang="ts"></script>

<template>
  <div class="timeline-conversation">
    <!--Message-->
    <div class="conversation-message">
      <div class="message-text">
        <div class="message-box primary">
          <p>
            The EIP-712 standard should be followed in the contract of the digital signature verifier.
          </p>
        </div>
        <span class="meta">John Doe</span>
      </div>
      <AvatarSimple picture="data:image/gif;base64,replace_with_your_image" size="medium" />
    </div>
    <!--Message-->
    <div class="conversation-message">
      <div class="message-text">
        <div class="message-box primary">
          <p>
            This looks good. Can you double check the test case of the wrong message format also?
          </p>
        </div>
        <span class="meta">John Doe</span>
      </div>
      <AvatarSimple picture="data:image/gif;base64,replace_with_your_image" size="medium" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.timeline-conversation {
  .conversation-message {
    display: flex;
    justify-content: flex-end;

    :deep(.avatar) {
      margin-top: auto;
    }

    .message-text {
      margin-right: 2rem;

      .message-box {
        padding: 1rem;
        border-radius: 1rem 1rem 0;
        font-family: var(--font);
        font-size: 0.9rem;
        line-height: 1.3;
        margin-bottom: 0.25rem;

        &.primary {
          background: var(--primary);
          color: var(--white-smoke);
        }

        &.secondary {
          background: var(--secondary);
          color: var(--white-smoke);
        }
      }

      .meta {
        display: block;
        text-align: right;
        margin-left: auto;
        font-family: var(--font);
        font-size: 0.9rem;
        color: var(--light-text);
      }
    }

    &:not(:last-child) {
      margin-bottom: 2rem;
    }
  }
}
</style>
