.PHONY: default clean hugo hugo-build

default: hugo

clean:
	rm -rf public/


hugo-build: clean hugo-themes
	hugo --enableGitInfo --source .

hugo:
	hugo server --disableFastRender --enableGitInfo --watch --source .
	# hugo server -D

hugo-themes:
	rm -rf themes
	mkdir themes
	git clone --depth=1 git@github.com:thingsym/hugo-theme-techdoc.git themes/hugo-theme-techdoc
	rm -rf themes/hugo-theme-techdoc/.git