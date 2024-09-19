Project-4 is to learn NextJS.

Tech/technical:



React-simplemde-editor: premade text input
React-hook-form: useForm (register, control,handleSubmit)
		Controller
axios: .post
useRouter() - next/navigation
@hookform/resolvers: react form to intergrate with various form validation library
zod: z.infer<typeof>

Radix-ui: Component library
import dynamic from 'next/dynamic'  
	- const simpleMDE = dynamic(()=> import('react-simplemde-editor'),{ssr:false})
	- this is to run client side component => LAZY LOADING
export const dynamic = 'force-dynamic' : opt out from static rendering
tanStack Query: query with cache

react-hot-toast : premade notification banner
rechard : charting library
Sentry: bug log


- npm i react-icons@4.11.0
- npm i classnames@2.3.2
- npm i prisma@5.3.1
- npm i zod@3.22.2
- npm install @radix-ui/themes
- npm install --save react-simplemde-editor easymde
- npm i axios@1.5.0 
- npm i @hookform/resolvers@3.3.1
- npm i delay   : simulate a slow server
- npm i react-loading-skeleton@3.3.1
- npm i react-markdown@8.0.7    : preview heading bold spacing inline text
- npm install -D @tailwindcss/typography
- npm i @radix-ui/react-icons 
- npm i @next-auth/prisma-adapter@1.0.7
- npm i @tanstack/react-query@4.35.3
- npm i react-hot-toast@2.4.1
- npm i recharts@2.8.0   


- npx prisma init
- npx prisma format
- npx prisma migrate dev
- python .\git-filter-repo.py --path .env --invert-paths --force
- npx @sentry/wizard@latest -i nextjs --url https://sentry.io





-------------------------
Structure: --------------
-------------------------


Vercel:
Build and output setting
	Build command: prisma generate && prisma migrate deploy && next build




NextRequest, NextResponse from "next/server"
	POST

validationSchemas:
	z.object

const {register, control, handleSubmit, formState: {error}} = useForm<IssueForm>({resolver:zodResover(createIssueSchema)})

<form onSubmit={handleSubmit(async data=> await axios.post("/api/issues", data) )}

ErrorMessage = ({children}:PropsWithChildren)
