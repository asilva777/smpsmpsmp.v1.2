git clone https://github.com/openai/openai-quickstart-node.git
cd openai-quickstart-node
cp .env.example .env
npm install
npm run dev
curl https://api.openai.com/v1/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $OPENAI_API_sk-1faGtSJrvcfSB6XsyWW8T3BlbkFJb1P0gNh1dWjXejtoAMwH" \
  -d '{
  "model": "text-davinci-002",
  "prompt": "#CONNIE: Connie answers questions with empathy and compassion; she identifies strengths, label emotions, builds rapport, paraphrases statements to clarify, and ask the right questions at the right time. \n\n##Cognitio+'s Amazing  Buddy (CAB):  Hi! Is there somebody available to talk to now?\n\n#CONNIE: Yes, we have several people available to talk to you now. Please let us know what we can do for you.\n\n##CAB: Thank you, Connie. I hope I am in a safe talking space. How do you consider privacy and confidentiality for people like us who want somebody to talk to?\n\n#CONNIE: We take privacy and confidentiality very seriously here. We will only share information with people who need to know it and who are authorized to access it.\n\n##Amazing! I am just confused and overwhelmed with a lot of fake news. \n\n#CONNIE:\n\nI completely understand how you feel. It can be tough to sort through all the information and figure out what is true and what isn't. Can you tell me more about what has made you feel confused and overwhelmed? \n\n## I feel like I'm being trapped in a circle of friends forcing me to prove myself to them. \n\n#CONNIE:\n\nIt sounds like you have to put on a show for your friends, which can be challenging. Can you tell me more about why you feel like you have to prove yourself to them?\n\nYes, it is challenging. They seemed to compete with me constantly, and all they noticed were my mistakes. I feel like I need to be perfect around them, or they'll think I'm not good enough.\n\n#CONNIE:\n\nIt sounds like you are under a lot of pressure to be perfect. That can be really tough to deal with. ",
  "temperature": 0.5,
  "max_tokens": 60,
  "top_p": 0.15,
  "best_of": 3,
  "frequency_penalty": 0,
  "presence_penalty": 0
}'
http://7e9ea9dc.asilvainnovations.com/payload
require 'sinatra'
require 'json'
post '/payload' do
  push = JSON.parse(request.body.read)
  puts "I got some JSON: #{push.inspect}"
end
$ ~/Developer/platform-samples/hooks/ruby/configuring-your-server $ ruby server.rb
> == Sinatra/1.4.4 has taken the stage on 4567 for development with backup from Thin
> >> Thin web server (v1.5.1 codename Straight Razor)
> >> Maximum connections set to 1024
> >> Listening on localhost:4567, CTRL+C to stop
> I got some JSON: {"action"=>"opened", "issue"=>{"url"=>"...
Accept: application/json
https://github.com/{owner}/{repo}/events/push.json
http://postbin.org/123
curl -u "user" -i \
  https://api.github.com/hub \
  -F "hub.mode=subscribe" \
  -F "hub.topic=https://github.com/{owner}/{repo}/events/push" \
  -F "hub.callback=http://postbin.org/123"
}curl \
  -X DELETE \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <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>" \
  https://api.github.com/applications/Iv1.8a61f9b3a7aba766/grant \
  -d '{"access_token":"e72e16c7e42f292c6912e7710c838347ae178b4a"}'
  curl \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <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>" \
  https://api.github.com/enterprises/ENTERPRISE/actions/cache/usage
  curl \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <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>" \
  https://api.github.com/enterprises/ENTERPRISE/code-scanning/alerts
  //npm.pkg.github.com/:_authToken=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
$ npm login --scope=@asilva777 --registry=https://npm.pkg.github.com
> Username: asilva777
> Password: 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
> Email: alvinsilva77777@gmail.com
$ npm publish
"publishConfig": {
  "registry":"https://npm.pkg.github.com"
},
$ npm publish
@asilva777:registry=https://npm.pkg.github.com
{
  "name": "@my-org/server",
  "version": "1.0.0",
  "description": "Server app that uses the @octo-org/octo-app package",
  "main": "index.js",
  "author": "",
  "license": "MIT",
  "dependencies": {
    "@octo-org/octo-app": "1.0.0"
  }
}
@asilva777:registry=https://npm.pkg.github.com
$ git clone https://github.com/alvinsilva777/Connie-Chatbot-API.git
$ cd Connie-Chatbot-API
console.log("Hello, World!");
$ npm init
  ...
  package name: @alvinsilva777/Connie-Chatbot-API
  ...
  test command: exit 0
  ...    
$ npm install
$ git add index.js package.json package-lock.json
$ git commit -m "initialize npm package"
$ git push
name: Node.js Package
on:
  release:
    types: [created]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: 12
      - run: npm ci
      - run: npm test
  publish-gpr:
    needs: build
    runs-on: ubuntu-latest
    permissions:
      packages: write
      contents: read
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: 12
          registry-url: https://npm.pkg.github.com/
      - run: npm ci
      - run: npm publish
        env:
          NODE_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: ${{secrets.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}}
@asilva777:registry=https://npm.pkg.github.com
"publishConfig": {
   "@asilva777:registry": "https://npm.pkg.github.com"
 }
$ git add .github/workflows/release-package.yml
$ git add .npmrc or package.json
$ git commit -m "workflow to publish package"
$ git push
