<template>
  <div id='list'>
    <div class="item clearfix" v-for="item in items" v-component="item">
      <div class="vote">
        <div class="total">
          {{ item.vote }}
        </div>
        <div class="action">
          <a href="#">&#x25B2;</a>
          <a href="#">&#x25BC;</a>
        </div>
      </div>
      <div class="content">
        {{ item.content }}
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'hello',
    data () {
      return {
        items: [
          {
            id: 1,
            vote: 3,
            content: 'Google starts tracking offline shopping – what you buy at stores in person ',
            timestamp: 1495599596265
          },
          {
            id: 2,
            vote: 1,
            content: 'Principal Component Analysis Explained Visually (2015) ',
            timestamp: 1495599790746
          },
          {
            id: 3,
            vote: 4,
            content: 'Uber Plans Millions in Back Pay After Shortchanging NYC Drivers',
            timestamp: 1495599802433
          },
          {
            id: 4,
            vote: 6,
            content: 'Dont use Hadoop when your data isnt that big (2013) ',
            timestamp: 1495599809888
          },
          {
            id: 5,
            vote: 7,
            content: 'Porting Windows Dynamic Link Libraries to Linux ',
            timestamp: 1495599818250
          },
          {
            id: 6,
            vote: 8,
            content: 'How a CEO with Dyslexia and ADHD Runs His Company ',
            timestamp: 1495599825249
          },
          {
            id: 7,
            vote: 9,
            content: '22-Year-Old Lidar Whiz Claims Breakthrough',
            timestamp: 1495599831961
          },
          {
            id: 8,
            vote: 1,
            content: 'Daryl Bem and the Replication Crisis',
            timestamp: 1495599838760
          },
          {
            id: 9,
            vote: 4,
            content: ' At The Dawn Of Recorded Sound, No One Cared ',
            timestamp: 1495599844624
          },
          {
            id: 10,
            vote: 12,
            content: 'Jamboard is now available ',
            timestamp: 1495599850938
          }

        ]
      }
    },
    components: {
      item: {
        computed: {
          count: () => {
            return this.upvote - this.downvote
          }
        }
      }
    }
  }
</script>
<style scoped>
#list .item {
  display: block;
  padding: 5px 0;
  width: 100vw;
}

#list .item .vote {
  width: 60px;
  border-radius: 5px;
  border: 1px solid #DDD;
  float: left;
}

#list .item .vote .total {
  line-height: 28px;
  text-align: center;
}

#list .item .vote .action {
  border-top: 1px solid #DDD;
  text-align: center;
}

#list .item .vote .action a {
  display: inline-block;
  color: #333;
  width: 20px;
  text-decoration: none;
}

#list .item .vote .action a:hover {
  color: #888;
}

#list .item .vote .action a:first-child {
  padding-right: 5px;
  border-right: 1px solid #DDD;
}

#list .item .content {
  padding-left: 0.5em;
  line-height: 28px;
  max-width: 80vw;
  float: left;
}

</style>
