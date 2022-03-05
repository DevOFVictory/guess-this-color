<template>
    <Page>
        <ActionBar backgroundColor="#8ff7eb">
            <Label text="Guess this color!" fontSize="24px"/>
        </ActionBar>

        <GridLayout backgroundColor="#d7fcf8">
            <Stacklayout>
                <GridLayout rows=auto columns=*,* backgroundColor="#b6faf2">
                    <FlexboxLayout row="0" column="0" class="time_flexbox">
                        <image height=55 width=55 src="res://time" stretch="aspectFit"/>
                        <label text="Time: 60s" class="score_time_label"/>

                    </FlexboxLayout>
                    <FlexboxLayout row="0" column="1" class="score_flexbox">
                        <label text="Score: 50" class="score_time_label"/>
                        <image height=55 width=55 src="res://score" stretch="aspectFit"/>
                    </FlexboxLayout>

                </GridLayout>
                <StackLayout height="2" width="90%" backgroundColor="Black"></StackLayout>
                <label fontSize="32px" textWrap="true" horizontalAlignment="center" style="text-align: center;">
                    <FormattedString>
                        <Span text="What is the " color="black"/>
                        <Span text="R" color="red" fontWeight="bold"/>
                        <Span text="G" color="green" fontWeight="bold"/>
                        <Span text="B" color="blue" fontWeight="bold"/>
                        <Span text="() " color="gray"/>
                        <Span text="value of " color="black"/>
                        <Span text="THIS" color="black" backgroundColor="yellow" fontStyle="italic"/>
                        <Span text=" color?" color="black"/>
                    </FormattedString>
                </label>
                <StackLayout height="2" width="90%" backgroundColor="Black"></StackLayout>
            </Stacklayout>
        </GridLayout>
    </Page>
</template>

<script>
  export default {
    computed: {
    }
  };
</script>

<style scoped lang="scss">
.time_flexbox {
    flex-direction: row;
    align-content: space-around;
    justify-content: flex-start;
    padding: 10
}
.score_flexbox {
    flex-direction: row;
    align-content: space-around;
    justify-content: flex-end;
    padding: 10;
}

.score_time_label {
    font-size: 20pt;
    vertical-align: center;
}

</style>
