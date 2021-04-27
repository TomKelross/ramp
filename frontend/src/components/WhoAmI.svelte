<section
    class="m-8 text-gray-600 bg-white border-8 border-t-8 body-font border-sblue"
>
    <div class="text-4xl text-white bg-sblue font-khand p2-3">Who are you?</div>
    <div class="container flex flex-col px-5 py-4 mx-auto text-lg text-black">
        <div class="w-full pb-2 lg:w-2/4">
            <p class="italic text-right gray-500">
                If you tell us a bit about yourself, we can show you more
                relevant information about the project. This information will
                only be stored locally.
            </p>
            <p>I am ...</p>
        </div>
        <div>
            <div class="pl-4">
                <div class="flex items-center mb-4 mr-4">
                    <input
                        id="iam1"
                        type="radio"
                        name="radio"
                        class="hidden"
                        checked
                    />
                    <label
                        for="iam1"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        A Person with access needs.</label
                    >
                </div>

                <div class="flex items-center mb-4 mr-4">
                    <input id="iam2" type="radio" name="radio" class="hidden" />
                    <label
                        for="iam2"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        A council worker or city planner
                    </label>
                </div>

                <div class="flex items-center mb-4 mr-4">
                    <input id="iam3" type="radio" name="radio" class="hidden" />
                    <label
                        for="iam3"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        A local business in a RAMP City</label
                    >
                </div>

                <div class="flex items-center mb-4 mr-4">
                    <input id="iam4" type="radio" name="radio" class="hidden" />
                    <label
                        for="iam4"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        A developer</label
                    >
                </div>

                <div class="flex items-center mb-4 mr-4">
                    <input id="iam5" type="radio" name="radio" class="hidden" />
                    <label
                        for="iam5"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        Choice Five with a longer title</label
                    >
                </div>
            </div>

            <p>I speak / Rydw'in siarad</p>
            <div class="pl-4">
                <div class="flex items-center mb-4 mr-4">
                    <input
                        id="ispeak1"
                        type="radio"
                        name="radio"
                        class="hidden"
                        checked
                    />
                    <label
                        for="ispeak1"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        English</label
                    >
                </div>

                <div class="flex items-center mb-4 mr-4">
                    <input
                        id="ispeak2"
                        type="radio"
                        name="radio"
                        class="hidden"
                    />
                    <label
                        for="ispeak2"
                        class="flex items-center text-xl cursor-pointer"
                    >
                        <span
                            class="inline-block w-8 h-8 mr-2 border rounded-full border-grey flex-no-shrink"
                        />
                        Cymru
                    </label>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    body {
        margin: 0;
        padding: 0;
        font-family: sans-serif;
    }

    input[type="radio"] + label span {
        transition: background 0.2s, transform 0.2s;
    }

    input[type="radio"] + label span:hover,
    input[type="radio"] + label:hover span {
        transform: scale(1.2);
    }

    input[type="radio"]:checked + label span {
        background-color: #0000fe;
        box-shadow: 0px 0px 0px 2px white inset;
    }

    input[type="radio"]:checked + label {
        color: #0000fe;
    }
</style>
