
  const SolanaPay = ({ recipient, splToken, amount}: Props)=>{

    const qr = useRef()
    useEffect(()=>{
      if (!recipient || !splToken || !amount) return
      const urlParams: TransferRequestURLFields = {
        recipient: new PublicKey(recipient),
        splToken: new PublicKey(splToken),
        amount: BigNumber(amount),
        reference,
        label,
        message,
      }
  
      const url = encodeURL(urlParams)
      const qr = createQR(url, 200, '#1B192F', "white")
      if (qrRef.current && amount > 0) {
        qrRef.current.innerHTML = ''
        qr.append(qrRef.current)
      }
    },[])
    return (
      <>
        <div ref={qr} />
      </>
    )
  }
  
