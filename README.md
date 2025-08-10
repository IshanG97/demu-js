# demu-js
Classifieds platform with bidding for Sri Lankan market

## Quick start
1. `cp .env.example .env.local`
2. `git config core.hooksPath .git/hooks`
3. Add the below to `.git/hooks/pre-commit`

```
#!/bin/sh
echo "🔍 Running ESLint before commit..."
npm run lint
RESULT=$?
if [ $RESULT -ne 0 ]; then
  echo "❌ ESLint failed. Commit aborted."
  exit 1
fi
echo "✅ ESLint passed. Proceeding with commit."
exit 0
```
4. Run the server
```bash
npm run dev
```