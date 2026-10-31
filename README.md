
"use client"
import { useState } from "react"

export default function SignupPage() {
  const [email, setEmail] = useState("")
  const [pass, setPass] = useState("")

  const handleSignup = async () => {
    // Ganti ini dengan Supabase / Clerk / API kamu nanti
    alert(`Akun dibuat untuk: ${email}`)
    // contoh redirect ke dashboard
    // window.location.href = "/dashboard"
  }

  return (
    <div className="min-h-screen bg-black text-white flex items-center justify-center">
      <div className="w-full max-w-md p-8 rounded-2xl border border-white/10 bg-white/[0.03]">
        <h1 className="text-2xl font-bold mb-1">Buat Akun Nexus</h1>
        <p className="text-sm text-white/50 mb-6">Akses dashboard beta kamu</p>
        
        <input 
          placeholder="Email" 
          value={email}
          onChange={e=>setEmail(e.target.value)}
          className="w-full mb-3 p-3 rounded-lg bg-white/5 border border-white/10 outline-none"
        />
        <input 
          placeholder="Password" 
          type="password"
          value={pass}
          onChange={e=>setPass(e.target.value)}
          className="w-full mb-4 p-3 rounded-lg bg-white/5 border border-white/10 outline-none"
        />
        <button onClick={handleSignup} className="w-full p-3 rounded-lg bg-white text-black font-semibold">
          Buat Akun
        </button>
        <p className="text-xs text-center text-white/40 mt-4">Sudah punya akun? <a href="/signin" className="text-white">Masuk</a></p>
      </div>
    </div>
  )
}
