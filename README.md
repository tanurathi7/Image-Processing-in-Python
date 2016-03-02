# Image-Processing-in-Python
//1)	TO PRINT IMAGE FORMAT, SIZE AND MODE AND DISPLAY IMAGE
import Image
Img = Image.open('Penguins.jpg')
print Img.format, Img.size, Img.mode
Img.show()

//2)	TO BLUR THE IMAGE
import Image
global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter		
	def filterBlur(im):
	    im1=im.filter(ImageFilter.BLUR)
	    im1.save("Penguins_BLUR"+ext)
	filterBlur(im1)

//3)	TO SHOW IMAGE CONTOURS
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterContour(im):
	    im1=im.filter(ImageFilter.CONTOUR)
	    im1.save("Penguins_CONTOUR"+ext)
	filterContour(im1)

//4)	TO CROP THE IMAGE
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	def imgCrop(im1):
		box=(200,300,400,500)
		region=im1.crop(box)
		region.save("Penguins_CROPPED"+ext)
	imgCrop(im1)

//5)	TO ENHANCE THE EDGES
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterEdgeEnhance(im):
	    im1=im.filter(ImageFilter.EDGE_ENHANCE)
	    im1.save("Penguins_EDGE_ENHANCE"+ext)
	filterEdgeEnhance(im1)

//6)	MORE EDGE ENHANCEMENT
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterEdgeEnhanceMore(im):
	    im1=im.filter(ImageFilter.EDGE_ENHANCE_MORE)
	    im1.save("Penguins_EDGE_ENHANCE_MORE"+ext)
	filterEdgeEnhanceMore(im1)

//7)	EMBOSS IMAGE
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterEmboss(im):
	    im1=im.filter(ImageFilter.EMBOSS)
	    im1.save("Penguins_EMBOSS"+ext)
	filterEmboss(im1)

//8)	TO FIND EDGES
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterFindEdges(im):
	    im1=im.filter(ImageFilter.FIND_EDGES)
	    im1.save("Penguins_EDGES"+ext)
	filterFindEdges(im1)

//9)	GREYSCALE
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	def bandMerge(im1):
	    r,g,b=im1.split()
	    im1=Image.merge("RGB",(g,g,g))
	    im1.save("Penguins_MERGE"+ext)
	bandMerge(im1)

//10)	TO SHARPEN THE IMAGE
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterSharpen(im):
	    im1=im.filter(ImageFilter.SHARPEN)
	    im1.save("Penguins_SHARPEN"+ext)
	filterSharpen(im1)

//11)	TO MAKE THE IMAGE SMOOTH
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterSmooth(im):
	    im1=im.filter(ImageFilter.SMOOTH)
	    im1.save("Penguins_SMOOTH"+ext)
	filterSmooth(im1)

//12)	TO MAKE THE IMAGE SMOOTHER
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	import ImageFilter
	def filterSmoothMore(im):
	    im1=im.filter(ImageFilter.SMOOTH_MORE)
	    im1.save("Penguins_SMOOTH_MORE"+ext)
	filterSmoothMore(im1)

//13)	TO TRANSPOSE/ROTATE A PART OF THE IMAGE
	import Image
	global ext
	ext=".jpg"
	imageFile="Penguins.jpg"
	im1=Image.open(imageFile)
	def imgTranspose(im1):
	    box=(200,300,400,500)
	    region=im1.crop(box)
	    region=region.transpose(Image.ROTATE_180)
	    im1.paste(region,box)
	    im1.save("Penguins_TRANSPOSE"+ext)
	imgTranspose(im1)
