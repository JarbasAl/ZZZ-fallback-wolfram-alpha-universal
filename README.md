## Universal Wolfram Alpha fallback
General knowledge fallback handler

## Description
Ask general-knowledge queries of your Mycroft device.  If no other skills can
handle the request, [Wolfram Alpha](https://wolframalpha.com) will be queried
to see if it can find an answer.  You'll be surprised by how much it knows!

For deeper exploration, you can also request the sources behind the answer.
An email will be sent to your registered account linking you to all the
details within Wolfram Alpha's website.

this version translates input into english and output into configured language

you should blacklist the official fallback-wolfram-alpha from your config file

## Examples
* "How tall is Mount Everest?"
* "When was The Rocky Horror Picture Show released?"
* "What is Madonna's real name?"
* "What's 18 times 4?"
* "How many inches in a meter?"
* "Send me the source on that" (info on the last query)

## LOGS

    03:02:40.868 - SKILLS - DEBUG - {"type": "recognizer_loop:utterance", "data": {"utterances": ["quando vai acabar o mundo"]}, "context": null}
    03:02:40.880 - mycroft.skills.padatious_service:handle_fallback:107 - DEBUG - Padatious fallback attempt: quando vai acabar o mundo
    03:02:40.890 - SKILLS - DEBUG - {"type": "mycroft.skill.handler.start", "data": {"handler": "fallback"}, "context": null}
    03:02:47.908 - mycroft_jarbas_utils.skills.auto_translatable:_universal_fallback_handler:128 - INFO - WolframAlphaSkill.handle_fallback
    03:02:47.908 - WolframAlphaSkill - DEBUG - WolframAlpha fallback attempt: When will the world end?
    03:02:47.908 - WolframAlphaSkill - DEBUG - Querying WolframAlpha: when will the world end?
    03:02:47.911 - SKILLS - DEBUG - {"type": "enclosure.mouth.think", "data": {}, "context": null}
    03:02:51.117 - SKILLS - DEBUG - {"type": "speak", "data": {"expect_response": false, "utterance": "5 bilhoes de anos, (O mundo acabara efetivamente com 5 bilhoes de anos a partir de agora, quando o Sol se tornar um gigante vermelho. Como um gigante vermelho, o Sol perdera aproximadamente 30% de sua massa e (sem efeitos de mare) a Terra se movera para um orbita 1,7 UA do Sol quando a estrela atinge o seu raio maximo. Portanto, espera-se que o planeta escape do envolvimento pela atmosfera externa dispersa do sol expandido, embora a maioria, se nao a totalidade, permaneca a vida sera destruida devido a maior luminosidade do Sol. No entanto, uma simulacao mais recente indica que a orbita da Terra ira decadir devido a efeitos de mare e arrastamento, fazendo com que ele entre na atmosfera do gigante vermelho do Sol e seja destruido.)", "metadata": null}, "context": {"target_lang": "pt", "auto_translated": true, "source_lang": "en"}}
    03:02:51.120 - SKILLS - DEBUG - {"type": "active_skill_request", "data": {"skill_id": 1423583182613266333}, "context": null}
    03:02:51.122 - SKILLS - DEBUG - {"type": "mycroft.skill.handler.complete", "data": {"handler": "fallback", "fallback_handler": "WolframAlphaSkill._universal_fallback_handler"}, "context": null}

## Credits
Mycroft AI
