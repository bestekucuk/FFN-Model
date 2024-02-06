import { client } from "@gradio/client";

const app = await client("https://bestekucuk-text-classfication.hf.space/--replicas/3epan/");
const result = await app.predict("/predict", [		
				"Hello!!", // string  in 'text' Textbox component
	]);

console.log(result.data);
